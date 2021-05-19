<template>
  <div class="app">
    <button @click="flipModalState">Click to fire modal</button>
    <br>
    <Modal :flipModalState="flipModalState"/>
  </div>
</template>

<script>
  import Modal from "./components/Modal.vue";

  export default {
    name: "App",
    components: {
      Modal,
    },
    methods: {
      flipModalState() {
        let x = document.getElementById("modalBookingComplete").style.display;
        document.getElementById("modalBookingComplete").style.display = x ? "" : "inline";
      }
    }
  };
</script>

<style lang="scss">
  body {
    background-color: #636f79;
    margin: 0;
  }
</style>
