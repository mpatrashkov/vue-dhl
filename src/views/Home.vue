<template>
  <div>
    <v-container>
      <v-stepper v-model="stepper" alt-labels>
        <v-stepper-header>
          <v-stepper-step :complete="stepper > 1" :step="1" editable>
            Produktauswahl
          </v-stepper-step>
          <v-divider></v-divider>
          <v-stepper-step :complete="stepper > 2" :step="2" editable>
            Warenkorb
          </v-stepper-step>
          <v-divider></v-divider>
          <v-stepper-step :complete="stepper > 3" :step="3" editable>
            Bezahlen
          </v-stepper-step>
          <v-divider></v-divider>
          <v-stepper-step :complete="stepper > 4" :step="4" editable>
            Ausdruck
          </v-stepper-step>
        </v-stepper-header>
      </v-stepper>
    </v-container>

    <v-container>
      <v-card>
        <v-card-title> DHL Online Frankierung </v-card-title>
        <v-tabs v-model="tab">
          <v-tab> Versandmarke </v-tab>
          <v-tab> Sparsets Kaufen </v-tab>
        </v-tabs>
      </v-card>
    </v-container>

    <v-tabs-items v-model="tab">
      <v-tab-item>
        <shipping-label />
      </v-tab-item>
      <v-tab-item>
        <bulk-shipping-label />
      </v-tab-item>
    </v-tabs-items>

    <app-footer />
  </div>
</template>

<script>
import AppFooter from "../components/AppFooter.vue";
import BulkShippingLabel from "../components/BulkShippingLabel.vue";
// @ is an alias to /src
import ShippingLabel from "../components/ShippingLabel.vue";

export default {
  name: "Home",
  data: () => ({
    stepper: 1,
    tab: null,
  }),
  components: {
    AppFooter,
    ShippingLabel,
    BulkShippingLabel,
  },
};
</script>

<style lang="scss"></style>
