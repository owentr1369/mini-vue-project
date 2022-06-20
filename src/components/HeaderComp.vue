<template>
  <div class="row">
    <div class="col-sm-12">
      <h3>Item Added</h3>
      <div class="progress">
        <div
          class="progress-bar progress-bar-success"
          role="progressbar"
          aria-valuenow="40"
          aria-valuemin="0"
          aria-valuemax="100"
          :style="{
            width: (itemCount / maxItem) * 100 + '%',
          }"
        ></div>
        {{ itemCount }}/{{ maxItem }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["itemCount", "maxItem"],
};
</script>

<style>
</style>