<template>
  <div class="row">
    <form action="">
      <div class="row">
        <div class="col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
          <label for="">Say...</label>
          <textarea
            class="form-group"
            name=""
            id=""
            cols="30"
            rows="10"
            v-model="item"
          ></textarea>
        </div>
      </div>
      <div class="row">
        <div class="col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
          <button class="btn btn-success" @click.prevent="createNew">
            Create New Item
          </button>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      item: "",
    };
  },
  methods: {
    createNew() {
      this.$emit("itemAdded", this.item);
      this.item = "";
    },
  },
};
</script>

<style scoped>
textarea {
  width: 100%;
  resize: none;
}
form {
  width: 100%;
}
</style>