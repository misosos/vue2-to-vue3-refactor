<!-- ParentComponent.vue -->
<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';
import {ref} from 'vue';

export default {
  name: "E05ParentComponent",
  components: { ChildComponent },

  setup(){
    const parentMessage = ref("Hello from parent");

    const handleEvent = (payload) => {
      console.log(payload);
    };

    return{
      parentMessage,
      handleEvent,
    };
  }

};
</script>
