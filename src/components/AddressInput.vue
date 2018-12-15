<template>
  <div>
    <h5>Address</h5>
    <div><input type="text" v-model="address.line1" @blur="onChange" /></div>
    <div><input type="text" v-model="address.city" @blur="onChange" /></div>
  </div>
</template>

<script>
export default {
  name: "AddressInput",
  props: {
    value: Object
  },
  data() {
    return {
      address: JSON.parse(JSON.stringify(this.value))
      // address: this.value
    };
  },
  methods: {
    onChange($event) {
      console.log("Event: ", $event.target.value, this.address);
      this.$emit("input", JSON.parse(JSON.stringify(this.address)));
    }
  }
};
</script>
