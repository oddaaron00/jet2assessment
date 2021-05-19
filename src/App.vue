<template>
  <div class="app">
    <h1>HI</h1>
    <button @click="flipModalState">Click to launch modal</button>
    <h2>HIII</h2>
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
    background-color: gray;
    margin: 0;
  }
</style>
