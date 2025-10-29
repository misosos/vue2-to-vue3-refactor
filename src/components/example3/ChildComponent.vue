<!-- ChildComponent.vue -->
<template>
  <div>
    <p>{{ message }}</p>
    <button @click="customEvent">Send Event</button>
  </div>
</template>

<script>

export default {
  props: ['message'],
  emits: ['custom-event'],

  setup(props, { emit }) {
    const customEvent = () => {
      emit('custom-event', 'Hello from child');
    };
    return {
      customEvent,
    }
  }
};
</script>
