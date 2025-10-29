<template>
  <div>
    <input v-model="message" />
    <p>{{ message }}</p>
  </div>
</template>

<script>
import  {ref} from "vue";
export default {
  name: "E03Binding",

  setup(){
    const message = ref("Hello Vue");
    return{
      message,
    };
  }
};
</script>
