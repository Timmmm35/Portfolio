<template>
  <div class="app">
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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;

}
#app{
  padding:0px;
}
.app {
  display: flex;
  flex-direction: column;
  justify-content:  left;
  width: 25vw;
  height: 100vh;
}
.heading-line {
  font-size: 50px;
  color: black;
}

</style>
