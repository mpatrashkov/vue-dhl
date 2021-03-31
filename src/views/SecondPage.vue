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
      <h2>Warenkorb</h2>

      <div class="py-2 card">
        <editable-product />
      </div>
      <div class="py-2 card">
        <editable-product />
      </div>

      <v-btn color="primary">Weitere Sendungen hinzufugen</v-btn>

      <v-card class="mt-2 card">
        <v-card-title>Coupon-Code einlosen</v-card-title>
        <div class="d-flex mx-3 pb-3">
          <v-text-field
            dense
            hide-details
            v-model="coupon"
            label="Code"
            outlined
            clearable
          ></v-text-field>
          <v-btn color="primary input-button" class="ml-3"> Einlosen </v-btn>
        </div>
      </v-card>

      <h2>Zahlungsart</h2>
      <v-radio-group v-model="paymentMethod">
        <payment-method
          class="card my-2"
          :value="0"
          @toggle="(value) => (paymentMethod = value)"
        />
        <payment-method
          class="card my-2"
          :value="1"
          @toggle="(value) => (paymentMethod = value)"
        />
        <payment-method
          class="card my-2"
          :value="2"
          @toggle="(value) => (paymentMethod = value)"
        />
      </v-radio-group>

      <v-btn color="primary">Jetzt zahlungspflichtig bestellen</v-btn>
    </v-container>

    <app-footer />
  </div>
</template>

<script>
import AppFooter from "../components/AppFooter.vue";
import EditableProduct from "../components/EditableProduct.vue";
import PaymentMethod from "../components/PaymentMethod.vue";

export default {
  components: { EditableProduct, AppFooter, PaymentMethod },
  name: "SecondPage",
  data: () => ({
    stepper: 2,
    coupon: "",
    paymentMethod: 0,
  }),
};
</script>

<style lang="scss" scoped>
.card {
  width: 600px;
}
button.input-button {
  height: unset !important;
}
</style>
