<template>
  <div class="row">
    <app-item
      v-for="(item, index) in items"
      :key="item"
      @click.native="removeItem(index)"
      >{{ item }}</app-item
    >
  </div>
</template>

<script>
import ItemsComp from "./ItemsComp.vue";
export default {
  props: ["items"],
  components: {
    appItem: ItemsComp,
  },
  methods: {
    removeItem(index) {
      this.$emit("itemRemove", index);
    },
  },
};
</script>