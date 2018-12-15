<template>
  <div>
    <h3>{{ pageTitle }}</h3>
    <section>
      <base-input v-model="customer.name"></base-input>
      <address-input v-model="customer.address"></address-input>
    </section>
    <section>
      Model:
      <p>{{ customer }}</p>
    </section>
  </div>
</template>

<script>
import BaseInput from "../components/BaseInput";
import AddressInput from "../components/AddressInput";

export default {
  name: "Page01",
  components: {
    BaseInput,
    AddressInput
  },
  data() {
    return {
      pageTitle: "Custom Component",
      customer: {
        name: "Name here...",
        address: {
          line1: "Park Station Road,",
          city: "Chennai"
        }
      }
    };
  }
};
</script>

<style scoped>
section {
  margin: 25px 15px;
}
</style>
