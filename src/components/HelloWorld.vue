<template>
  <div class="hello-world">
    <h2>{{ message }}</h2>
    <button @click="sendToApp">Send message to App</button>
    <slot></slot>  <!-- Slot for default content passed from parent -->
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  methods: {
    sendToApp() {
      this.$emit('sendMessage', 'Hello from HelloWorld component!');
    },
  },
};
</script>

<style scoped>
.hello-world {
  background-color: #f4f4f4;
  padding: 10px;
}
</style>
