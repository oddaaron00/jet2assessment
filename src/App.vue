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
        let y = document.getElementById("modal--booking-complete").style.display;
        document.getElementById("modal--booking-complete").style.display = y ? "" : "inline";
      }
    }
  };
</script>

<style lang="scss">
  #dimmer
  {
      background:#000;
      opacity:0.5;
      position:fixed; /* important to use fixed, not absolute */
      top:0;
      left:0;
      width:100%;
      height:100%;
      z-index:9999; /* may not be necessary */
  }

  body {
    background-color: #636f79;
    margin: 0;
  }
</style>
