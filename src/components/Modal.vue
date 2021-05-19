<template>
  <div class="modal" id="modalBookingComplete">
    <div class="modal__container modal__container--main">
      <header class="modal__header">
          <font-awesome-icon class="modal__img modal__img--icon" icon="check-circle"/>
          <h1 class="modal__text modal__text--heading">
            Congratulations! Your Jet2 holiday booking has been confirmed.
          </h1>
      </header>
      <main class="modal__body">
        <p class="modal__text modal__text--body">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consectetur inventore, dignissimos quasi fuga sunt, nihil nemo labore? Molastiae, eum, eos! Illum non laborum asperiores, mollitia minima quasi atque. Eligendi, atque.</p>
      </main>
      <hr class="hr">
      <footer class="modal__footer">
        <button @click="flipModalState" class="modal__button modal__button--cancel">Cancel</button>
        <button @click="flipModalState" class="modal__button modal__button--continue">Continue</button>
      </footer>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Modal",
    props: {
      flipModalState: Function
    }
  };
</script>

<style lang="scss">
  @use "../assets/globals";

  /*
  .modal {
    background-color: #f2f2f2;
    position: fixed;
    bottom: 0;
    width: 100%;

    .modal__container--main {
      margin: auto;
      width: 88%;
    }

    .hr {
    }

    .modal__header {
      padding-top: 14px;
      display: flex;
      flex-direction: row;

      .modal__img--icon {
        color: #098c09;
        font-size: 3.5vh;
        padding-right: 12px;
        padding-top: 9px;
      }

      .modal__text--heading {
        font-family: globals.$font-stack;
        font-size: 3.3vh;
      }

    }

    .modal__body {
        .modal__text--body {
          padding-bottom: 12px;
          font-family: globals.$font-stack;
          font-size: 2.5vh;
        }
      }

      .modal__footer {
        display: flex;
        flex-direction: column;

        .modal__button--cancel {
          border: 3px solid globals.$secondary-color;
          border-radius: 5px;
          width: 100%;
          height: 45px;
          color: globals.$secondary-color;
          font-size: 2.56vh;
          font-weight: bolder;
          font-style: italic;
          margin: 2px auto;
        }

        .modal__button--continue {
          background-color: globals.$primary-color;
          border-radius: 5px;
          width: 100%;
          height: 45px;
          color: #f2f2f2;
          margin: 2px auto;
          font-size: 2.56vh;
          font-weight: bolder;
          font-style: italic;
          margin-bottom: 9px;
        }
      }
  }
  */

  .modal {
    display: none;
    background-color: #f2f2f2;
    position: fixed;
    bottom: 0;
    width: 100%;

    &__container {
      &--main {
        margin: auto;
        width: 88%;
      }
    }

    .hr {
    }

    &__header {
      padding-top: 14px;
      display: flex;
      flex-direction: row;
    }

    &__img {
      &--icon {
        color: #098c09;
        font-size: 3.5vh;
        padding-right: 12px;
        padding-top: 9px;
      }
    }

    &__text {
      font-family: globals.$font-stack;

      &--heading {
        font-size: 3.3vh;
      }

      &--body {
        padding-bottom: 12px;
        font-size: 2.5vh;
      }
    }

    &__footer {
      display: flex;
      flex-direction: column;
    }

    &__button {
        border-radius: 5px;
        width: 100%;
        font-size: 2.56vh;
        font-weight: bolder;
        font-style: italic;
        height: 45px;

      &--cancel {
        border: 3px solid globals.$secondary-color;
        color: globals.$secondary-color;
        margin: 2px auto;
      }

      &--continue {
        background-color: globals.$primary-color;
        color: #f2f2f2;
        margin: 2px auto;
        margin-bottom: 9px;
      }
    }
  }
</style>