<template>
  <div>Hello, {{ message }}</div>
</template>

<script>
import {ref} from "vue";
export default {
  name: "E01Instance",
  setup() {
    const message = ref("Vue!");
    return{
      message,
    };
  }
};
</script>

<style scoped>
div {
  color: blue;
}
</style>
