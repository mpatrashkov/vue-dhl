<template>
  <v-card @click="toggle">
    <div class="d-flex align-center justify-space-between">
      <div class="ma-3 d-flex align-center">
        <v-radio class="ma-0"></v-radio>
        <div class="text-h6">Bitcoin</div>
      </div>
      <img
        src="https://www.paypalobjects.com/webstatic/en_US/i/buttons/PP_logo_h_150x38.png"
        alt="PayPal"
        style="height: 38px"
        class="mx-3"
      />
    </div>
  </v-card>
</template>

<script>
export default {
  name: "PaymentMethod",
  props: {
    value: Number,
  },
  methods: {
    toggle() {
      this.$emit("toggle", this.value);
    },
  },
};
</script>
