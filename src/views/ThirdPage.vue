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
      <v-card class="card">
        <v-card-title> Ausdruck </v-card-title>
        <div class="pa-3">
          <div>Ihre Auftrags</div>
          <v-chip class="text-body-1 px-5">
            DKF9SMOQ55
            <v-icon right class="pl-2"> mdi-content-copy </v-icon>
          </v-chip>

          <div>Ihre Auftrags</div>
          <v-chip class="text-body-1">
            https://example.com?data=DKF9SMOQ55
            <v-icon right class="pl-2"> mdi-content-copy </v-icon>
          </v-chip>
        </div>
      </v-card>

      <v-card class="card">
        <v-card-title> Paket national, 10kg </v-card-title>
        <v-card-text>
          <div>Alle Etiketen als PDF Downloaden (A5)</div>
          <div>Alle Etiketen als PDF Downloaden (A5)</div>
          <div>Alle Etiketen als PDF Downloaden (A5)</div>
          <div>Alle Etiketen als PDF Downloaden (A5)</div>
        </v-card-text>

        <v-card-text>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
          <div class="d-flex">
            <div class="font-weight-bold">Artikel-ID: JJ1234567890123456</div>
            <div class="ml-5">HERUNTERLADEN</div>
          </div>
        </v-card-text>
      </v-card>
    </v-container>

    <app-footer />
  </div>
</template>

<script>
import AppFooter from "../components/AppFooter.vue";
export default {
  components: { AppFooter },
  name: "ThirdPage",
  data: () => ({
    stepper: 4,
  }),
};
</script>

<style lang="scss" scoped>
.card {
  width: 600px;
}
</style>
