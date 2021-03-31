<template>
  <v-container>
    <v-card>
      <v-card-title> Versandmarke - Sparsets </v-card-title>
      <v-card-text>
        <div>Spar bis zu 30% der Versandkosten</div>
        <div>
          <a>So funktioniert's</a>
        </div>
      </v-card-text>
    </v-card>

    <v-card class="mt-3">
      <v-card-title> Zielland wahlen </v-card-title>
      <v-card-text>
        <v-radio-group>
          <v-radio label="Deutschland" />
          <v-radio label="EU" />
        </v-radio-group>
      </v-card-text>
    </v-card>

    <h2 class="mt-3">Sparset zusammenstellen</h2>
    <v-card class="mt-3">
      <bulk-products />
    </v-card>
  </v-container>
</template>

<script>
import BulkProducts from "./BulkProducts.vue";
export default {
  components: { BulkProducts },
  name: "BulkShippingLabel",
};
</script>
