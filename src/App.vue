<template>
  <div id="app">
    <app-header :item-count="items.length" :max-item="maxItem"></app-header>
    <app-new-item @itemAdded="addItem" :items="items"></app-new-item>
    <app-items-layout
      :items="items"
      @itemRemove="removeItem"
    ></app-items-layout>
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
import HeaderComp from "./components/HeaderComp.vue";
export default {
  name: "App",
  components: {
    appItemsLayout: ItemsLayout,
    appNewItem: NewItem,
    appHeader: HeaderComp,
  },
  data: function () {
    return {
      items: [],
      maxItem: 10,
    };
  },
  methods: {
    addItem(item) {
      if (this.items.length >= this.maxItem) {
        return alert("Please remove 1 item first");
      }

      this.items.push(item);
    },
    removeItem(index) {
      this.items.splice(index, 1);
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
