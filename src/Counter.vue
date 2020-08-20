<template>
  <div>
    <button :click="upFuntion" class="btn btn-info">{{ label }}</button>
    <p v-bind:style="{fontSize: fsize + 'px'}">HELLO {{ counter }}></p>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fsize: 50,
    };
  },
  props: {
    label: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 1;
      this.fsize += 10;

      console.log(this.fsize);
      console.log(this.counter);
    },
  },
}
</script>

<style>
</style>