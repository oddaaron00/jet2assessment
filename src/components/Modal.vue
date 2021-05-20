<template>
  <div class="modal" id="modal--booking-complete">
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
        font-size: 16pt;
        color: globals.$primary-color;
      }

      &--body {
        padding-bottom: 12px;
        font-size: 12pt;
        color: globals.$secondary-color;
      }
    }

    &__footer {
      display: flex;
      flex-direction: column;
    }

    &__button {
      cursor: pointer;
        border-radius: 5px;
        width: 100%;
        font-size: 16px;
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

  @media screen and (min-width: 641px) {
    .modal {
      max-width: 800px;
      position: fixed;
      bottom: initial;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);


      &__container {
        &--main {
        }
      }

      .hr {
      }

      &__header {
        padding: 0px 30px;
        padding-top: 60px;
      }

      &__img {
        padding-top: 12px;
        padding-right: 20px;
        &--icon {
        }
      }

      &__text {

        &--heading {
          font-size: 20pt;
        }

        &--body {
          padding: 0px 30px;
          font-size: 13.8pt;
          padding-bottom: 35px;
        }
      }

      &__footer {
        flex-direction: row;
        justify-content: center;
        padding: 15px 0px;
      }

      &__button {
        width: 30%;
        margin-left: 2px;
        margin-right: 2px;

        &--cancel {
        }

        &--continue {
        }
      }
    }
  }
</style>