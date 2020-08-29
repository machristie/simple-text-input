<template>
  <!-- .stop added to prevent native InputEvent from being dispatched along
  with custom 'input' event -->
  <input type="text" :value="value" @input.stop="onInput" />
</template>

<script>
export default {
  name: "simple-text-input",
  props: {
    value: {
      type: String,
      required: true,
    },
  },
  methods: {
    onInput(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>

<style>
input {
  width: 100%;
  background-color: lightgreen;
}
</style>
