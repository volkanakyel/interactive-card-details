<script setup>
import CreditCard from "./components/CreditCard.vue";
import InteractiveForm from "./components/InteractiveForm.vue";
</script>

<template>
  <div class="left-container">
    <CreditCard class="credit-card-front" />
    <CreditCard class="credit-card-back" :frontCard="false" />
  </div>
  <section class="right-container">
    <InteractiveForm />
  </section>
</template>

<style lang="scss" scoped>
.left-container {
  background-image: url("./assets/images/bg-main-desktop.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
  width: 32%;
  max-width: 483px;
  @media (max-width: 1080px) {
    background-image: url("./assets/images/bg-main-mobile.png");
    width: 100%;
    max-width: 100%;
    min-height: 30vh;
  }
}
.right-container {
  width: 68%;
  margin: auto auto;
  @media (max-width: 1080px) {
    width: 100%;
    margin: auto auto;
    margin-top: 140px;
  }
}
.credit-card-front {
  position: absolute;
  top: 15%;
  right: -30%;
  z-index: 999;
  @media (max-width: 1080px) {
    top: 57%;
    left: 4%;
  }
}
.credit-card-back {
  position: absolute;
  top: 50%;
  right: -45%;
  z-index: 998;
  @media (max-width: 1080px) {
    top: 10%;
    right: 4%;
  }
}
</style>
