<template>
  <div>
    <v-card-title> Pakete national </v-card-title>

    <v-container>
      <div class="products">
        <product />
        <product />
        <product />
        <product />
        <product />
        <product />
      </div>
    </v-container>

    <div>Alle Preise</div>
  </div>
</template>

<script>
import Product from "./Product.vue";
export default {
  components: { Product },
  name: "ProductRow",
};
</script>
