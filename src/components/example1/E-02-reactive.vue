<template>
  <div>{{ fullName() }}</div>
</template>

<script>
import {onMounted, ref} from "vue";

export default {
  name: "E02Reactive",

  setup(){
    const firstName = ref("Kyungsu");
    const lastName = ref("Lee");

    const fullName = () => {
      return firstName.value + " " + lastName.value;
    }

    onMounted(() => {
      setTimeout(() => {
        firstName.value = "KSL";
      }, 2000);
    });

    return {
      firstName,
      lastName,
      fullName,
    };
  }
};
</script>
