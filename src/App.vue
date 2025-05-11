<template>
  <div id="app">
    <h1>Vue.js Tutorial Example</h1>
    <HelloWorld :message="messageFromApp" @sendMessage="handleMessage" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data() {
    return {
      messageFromApp: 'Hello from App Component!',
    };
  },
  methods: {
    handleMessage(message) {
      alert(message);
    },
  },
};
</script>
