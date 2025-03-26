<template>
  <div id="app">
    <h1>Welcome to My Portfolio</h1>
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
  text-align: center;
  margin-top: 50px;
}
</style>
