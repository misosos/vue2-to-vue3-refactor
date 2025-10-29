<!-- ChildComponent.vue -->
<template>
  <div>
    <p>{{ sharedMessage }}</p>
  </div>
</template>

<script>
import {inject} from "vue";

export default {

  setup() {
    const sharedMessage = inject("sharedMessage");

    return{
      sharedMessage,
    };
  }

};
</script>

<style scoped>
  p {
    font-size: 1.5rem;
  }
</style>
