<template>
  <div id="app">
    <app-items-layout></app-items-layout>
  </div>
</template>

<script>
import ItemsLayout from "./components/ItemsLayout.vue";
export default {
  name: "App",
  components: { appItemsLayout: ItemsLayout },
  data: function () {
    return {
      items: ["Good morning"],
      maxItems: 10,
    };
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
  margin-top: 60px;
}
</style>
