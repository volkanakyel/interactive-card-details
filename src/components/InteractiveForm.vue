<template>
  <div v-if="1" class="interactive-form">
    <label for="">Cardholder Name</label>
    <input class="base-input" type="tel" placeholder="e.g. Jane Appleseed" />
    <label for="ccn">Card Number</label>
    <input
      id="ccn"
      class="base-input"
      type="text"
      pattern="[0-9]*"
      inputmode="numeric"
      autocomplete="cc-number"
      maxlength="19"
      placeholder="e.g. 1234 5678 9123 0000"
    />
    <label for="">Exp. Date (MM/YY)</label>
    <div class="exp-date">
      <input
        class="num-input"
        type="text"
        placeholder="MM"
        pattern="[0-9]*"
        inputmode="numeric"
      />
      <input
        class="num-input"
        type="text"
        placeholder="YY"
        pattern="[0-9]*"
        inputmode="numeric"
      />
      <input
        class="cvv-input"
        type="text"
        placeholder="e.g. 123"
        pattern="[0-9]*"
        inputmode="numeric"
      />
    </div>
    <button>Confirm</button>
  </div>
  <div v-else class="success-message">
    <img src="../assets/images/icon-complete.svg" alt="" />
    <h2>Thank you!</h2>
    <p>We've added your card details</p>
    <button>Continue</button>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.success-message {
  width: 380px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  img {
    margin-bottom: 36px;
  }
  h2 {
    margin: 0;
    font-weight: 500;
    font-size: 28px;
    line-height: 36px;
    letter-spacing: 3.42222px;
    text-transform: uppercase;
  }
  p {
    color: #8f8694;
    margin-bottom: 48px;
    font-size: 18px;
  }
}
.interactive-form {
  max-width: 380px;
  font-size: 18px;
  margin: 0 auto;
  .base-input:not(:last-child) {
    margin-bottom: 26px;
  }
  label:not(:last-child) {
    margin-bottom: 9px;
  }
}
label {
  display: block;
}
button {
  width: 100%;
  display: block;
}

.base-input {
  width: 380px;
  padding: 12px;
  border: 1px solid #dfdee0;
  background: #fff;
  border-radius: 8px;
  color: #21092f;
  &:focus-visible {
    outline: none;
  }
}
.num-input {
  width: 80px;
  padding: 12px;
  border: 1px solid #dfdee0;
  border-radius: 8px;
  background: #fff;
  color: #21092f;
  &:focus-visible {
    outline: none;
  }
}
.exp-date {
  display: flex;
  justify-content: space-between;
  margin-bottom: 40px;
}

.cvv-input {
  width: 191px;
  padding: 12px;
  border: 1px solid #dfdee0;
  border-radius: 8px;
  background: #fff;
  color: #21092f;
  &:focus-visible {
    outline: none;
  }
}
</style>
