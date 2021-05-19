<template>
  <div class="modal__container">
    <div class="modal">
      <header class="modal__header">
        <font-awesome-icon icon="check-circle"/>
        <h1 class="modal__text modal__text--heading">
          Congratulations! Your Jet2 holiday booking has been confirmed.
        </h1>
      </header>
      <main class="modal__body">
        <p class="modal__text modal__text--para">Lorem ipsum</p>
      </main>
      <footer class="modal__footer">
        <button class="modal__button modal__button--cancel">Cancel</button>
        <button class="modal__button modal__button--continue">Continue</button>
      </footer>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
};
</script>

<style lang="scss">
@use "../assets/globals";

.modal {
    &__container {
        background-color: white;
        position: fixed;
        bottom: 0;
        width: 100%;
    }

    &__text {
        font-family: globals.$font-stack;

        &--heading {
            color: globals.$primary-color;
        }

        &--para {
            color: globals.$secondary-color;
        }
    }
}
</style>