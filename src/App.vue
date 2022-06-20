<template>
  <div id="app">
    <app-new-item @itemAdded="addItem"></app-new-item>
    <app-items-layout :items="items"></app-items-layout>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on item to delete it</div>
      </div>
    </div>
  </div>
</template>

<script>
import ItemsLayout from "./components/ItemsLayout.vue";
import NewItem from "./components/NewItem.vue";
export default {
  name: "App",
  components: { appItemsLayout: ItemsLayout, appNewItem: NewItem },
  data: function () {
    return {
      items: [],
      maxItems: 10,
    };
  },
  methods: {
    addItem(item) {
      this.items.push(item);
    },
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
  margin-top: 80px;
  width: 80%;
}
</style>
