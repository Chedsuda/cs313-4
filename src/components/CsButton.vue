<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-primary">Terrific {{lable}}</button>
    <button v-on:click="downFunction" class="btn btn-warning ml-3">Terrible {{lable}}</button>
    <button v-on:click="LoveFunction" class="btn btn-primary ml-3">Love {{lable}}</button>
    <button v-on:click="ResetFunction" class="btn btn-warning ml-3">Reset {{lable}}</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -5;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>