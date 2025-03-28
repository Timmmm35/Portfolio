<template>
    <canvas ref="threeCanvas"></canvas>
  </template>
  
  <script>
  import * as THREE from "three";
  import { onMounted, ref } from "vue";
  
  export default {
    setup() {
      const threeCanvas = ref(null);
  
      onMounted(() => {
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ canvas: threeCanvas.value });
        renderer.setSize(window.innerWidth, window.innerHeight);
        document.body.appendChild(renderer.domElement);
        //Cube
        const geometry = new THREE.BoxGeometry();
        const material = new THREE.MeshPhongMaterial({ color: 0x00ff00 });
        const cube = new THREE.Mesh(geometry, material);
        scene.add(cube);
        //Lighting
        const AmbientLight = new THREE.AmbientLight( 0x404040 ); // soft white light
        const color = 0xFFFFFF;
        const intensity = 3;
        const light = new THREE.DirectionalLight(color, intensity);
        light.position.set(-1, 2, 4);
        scene.add(light);
        scene.add( AmbientLight );
  
        camera.position.z = 5;
  
        function animate() {
          requestAnimationFrame(animate);
          cube.rotation.x += 0.01;
          cube.rotation.y += 0.01;
          renderer.render(scene, camera);
        }
        animate();
      });
  
      return { threeCanvas };
    },
  };
  </script>
  
  <style>
  canvas {
    display: block;
  }
  </style>
  