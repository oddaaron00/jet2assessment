<template>
  <div class="app">
    <div id="dimmer" class=""></div>
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
        const x = document.getElementById("dimmer").className;
        if (x.indexOf("dimmed") !== -1) {
          document.getElementById("dimmer").className = x.replace(" dimmed", "");
        } else {
          document.getElementById("dimmer").className += " dimmed";
        }

        // Get display property of modal--booking-complete's style object
        const y = document.getElementById("modal--booking-complete").style.display;
        // If y is truthy (i.e. has a value other than "none"), make it not display. Otherwise, make it display inline
        document.getElementById("modal--booking-complete").style.display = y ? "" : "inline";
      }
    }
  };
</script>

<style lang="scss">
  .dimmed
  {
      background:#000;
      opacity:0.5;
      position:fixed;
      top:0;
      left:0;
      width:100%;
      height:100%;
      z-index:9999;
  }

  body {
    background-color: #636f79;
    margin: 0;
  }
</style>
