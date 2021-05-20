<template>
  <div class="app" id="root">
    <div id="dimmer" class=""></div>
    <button @click="fireModal">Click to fire modal</button>
    <br>
    <modal v-for="modal in modals" :key="modal" :closeModal="closeModal"/>
  </div>
</template>

<script>
  import modal from "./components/Modal.vue";

  function fireModal() {
    const renderComponent = {
      render (h) {         
        return h(modal, {
          props: {
            closeModal: Function
          }
        });
      }
    }

    this.modals.push(renderComponent);
  }

  function closeModal() {
    this.modals.pop();
  }

  export default {
    name: "App",
    components: {
      modal,
    },
    data() {
      return {
        modals: []
      }
    },
    methods: {
      fireModal,
      closeModal
    }
  };
</script>

<style lang="scss">
  body {
    background-color: #636f79;
    margin: 0;
  }
</style>
