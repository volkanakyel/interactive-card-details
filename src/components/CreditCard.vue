<template>
  <div v-if="frontCard" class="front-card">
    <div class="front-card__label">
      <div class="circle-big"></div>
      <div class="circle-small"></div>
    </div>
    <div class="front-card__number">9591 6489 6389 1011</div>
    <div class="front-card__info">
      <span class="name">JANE APPLESEED</span>
      <span class="date">00/00</span>
    </div>
  </div>
  <div v-else class="back-card">
    <div class="back-card__header">
      <div class="black-banner"></div>
    </div>
    <div class="back-card__content">
      <div class="back-card__ccv">
        <span>000</span>
      </div>
      <img
        class="back-card__encryption"
        src="../assets/images/encryption-card.svg"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    frontCard: {
      type: Boolean,
      default: true,
    },
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.front-card {
  width: 447px;
  background: linear-gradient(163.95deg, #6348fe 4.74%, #610595 88.83%);
  color: #fff;
  font-weight: 600;
  letter-spacing: 3.42222px;
  padding: 32px;
  border-radius: 10px;
  @media (max-width: 1080px) {
    width: 286px;
    padding: 16px 18px;
  }
  &__label {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-bottom: 55px;
    @media (max-width: 1080px) {
      margin-bottom: 37px;
    }
  }
  &__number {
    display: flex;
    font-size: 28px;
    line-height: 36px;
    margin-bottom: 26px;
    @media (max-width: 1080px) {
      font-size: 18px;
      margin-bottom: 17px;
    }
  }
  &__info {
    display: flex;
    justify-content: space-between;
  }
}

.back-card {
  width: 447px;
  color: #fff;
  font-weight: 600;
  letter-spacing: 3.42222px;
  border-radius: 10px;
  background: linear-gradient(168.73deg, #ffffff 5%, #d2d3d9 91.69%);
  @media (max-width: 1080px) {
    width: 286px;
  }
  &__header {
    padding-top: 23px;
    margin-bottom: 23px;
    @media (max-width: 1080px) {
      padding-top: 14px;
      margin-bottom: 14px;
    }
  }
  &__content {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    @media (max-width: 1080px) {
      margin-top: 0;
    }
  }
  &__ccv {
    max-width: 80%;
    display: flex;
    justify-content: flex-end;
    padding: 10px 6px;
    background: #adb5be;
    width: 361px;
    border-radius: 6px;
    margin-inline: 45px;
    @media (max-width: 1080px) {
      margin-bottom: 45px;
    }
  }
  &__encryption {
    margin: 33px 0 47px 0;
    @media (max-width: 1080px) {
      display: none;
    }
  }
}
</style>
