<!-- ParentComponent.vue -->
<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script>

import ChildComponent1 from "@/components/example4/ChildComponent1.vue";
import {provide} from "vue";
import {ref} from "vue";
export default {
  name: "E06ParentComponent",
  components: {ChildComponent1},
  setup(){
    const sharedMessage = ref("Hello from provide");

    provide('sharedMessage', sharedMessage);

  }
};
</script>
