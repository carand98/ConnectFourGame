<template>
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <GridTable/>

</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import GridTable from "@/components/GridTable.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    GridTable
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
}
</style>
