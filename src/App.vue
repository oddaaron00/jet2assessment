<template>
  <div class="app">
    <h1>HI</h1>
    <button @click="modal = !modal">Click to launch modal</button>
    <h2>HIII</h2>
    <Modal v-show="modal"/>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

const greet = () => alert("HI");

export default {
  name: "App",
  components: {
    Modal,
  },
  methods: {
    greet,
  },
  data() {
    return {
      modal: false,
    };
  },
};
</script>

<style lang="scss">
body {
  background-color: gray;
  margin: 0;
}
</style>
