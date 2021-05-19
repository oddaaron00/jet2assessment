<template>
  <div class="modal">
    <div class="main-container">
      <header class="header">
          <font-awesome-icon class="img" icon="check-circle"/>
          <h1 class="heading">
            Congratulations! Your Jet2 holiday booking has been confirmed.
          </h1>
      </header>
      <main class="body">
        <p class="body-text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consectetur inventore, dignissimos quasi fuga sunt, nihil nemo labore? Molastiae, eum, eos! Illum non laborum asperiores, mollitia minima quasi atque. Eligendi, atque.</p>
      </main>
      <footer class="footer">
        <button class="cancel-button">Cancel</button>
        <button class="continue-button">Continue</button>
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
  background-color: #f2f2f2;
  position: fixed;
  bottom: 0;
  width: 100%;

  .main-container {
    margin: auto;
    width: 88%;
  }

  .header {
    padding-top: 14px;
    display: flex;
    flex-direction: row;

    .img {
      color: #098c09;
      font-size: 3.5vh;
      padding-right: 12px;
      padding-top: 9px;
    }

    .heading {
      font-family: globals.$font-stack;
      font-size: 3.3vh;
    }

  }

  .body {
      .body-text {
        font-family: globals.$font-stack;
        font-size: 2.5vh;
      }
    }

    .footer {
      display: flex;
      flex-direction: column;

      .cancel-button {
        border: 3px solid globals.$secondary-color;
        border-radius: 5px;
        width: 100%;
        height: 45px;
        color: globals.$secondary-color;
        font-size: 2.56vh;
        font-weight: bolder;
        font-style: italic;
        margin: 1px auto;
      }

      .continue-button {
        background-color: globals.$primary-color;
        border-radius: 5px;
        width: 100%;
        height: 45px;
        color: #f2f2f2;
        margin: 1px auto;
        font-size: 2.56vh;
        font-weight: bolder;
        font-style: italic;
        margin-bottom: 9px;
      }
    }
}
</style>