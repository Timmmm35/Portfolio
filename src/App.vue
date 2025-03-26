<template>
  <div id="app">
    <h1 class="heading-line">Welcome to My Portfolio</h1>
    <h3 id="author-line">brought to you by: Dequan Brown</h3>
    <button>Click to continue</button>
    <ThreeScene />
  </div>
</template>

<script>
import ThreeScene from "./components/ThreeScene.vue";

export default {
  components: { ThreeScene },
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  justify-content:  left;
  align-content: top;
  width: 30vw;
  height: 100vh;
}
.heading-line {
  font-size: 50px;
  margin-left: 50px;
  margin-top: 50px;
  color: black;
}

</style>
