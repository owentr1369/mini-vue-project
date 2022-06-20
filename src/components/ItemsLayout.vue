<template>
  <div class="row">
    <app-item v-for="item in items" :key="item">{{ item }}</app-item>
  </div>
</template>

<script>
import ItemsComp from "./ItemsComp.vue";
export default {
  props: ["items"],
  components: {
    appItem: ItemsComp,
  },
};
</script>