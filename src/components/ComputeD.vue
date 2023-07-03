<template>
  <h1>Computed in vue</h1>
  <label for="amount">amount</label>
  <input
    v-on:change="toggler = true"
    type="text"
    name="amount"
    id="amount"
    v-model.lazy="amount"
  />
  <h2 v-if="toggler">
    Your converted amount in rupees{{ getConvertedAmount }}
  </h2>
  <h2 v-else>Result</h2>
</template>
<script>
export default {
  name: "ComputeD",
  data() {
    return {
      rupeeToDoller: 80,
      discount: 10,
      inputAmount: null,
      toggler: false,
      amount: null,
    };
  },
  computed: {
    getConvertedAmount() {
      return this.amount * this.rupeeToDoller - 10 / 100;
    },
  },
};
</script>
