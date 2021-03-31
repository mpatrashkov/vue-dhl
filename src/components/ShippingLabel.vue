<template>
  <v-container>
    <v-card>
      <v-card-title> Produktauswahl </v-card-title>

      <v-card-text> Hier geht's zum Mengenrabatt </v-card-text>

      <product-row />
      <product-row />
    </v-card>

    <v-card>
      <v-card-text>
        <v-container>
          <div class="row">
            <div class="left">Summe</div>
            <div class="right">3,90€</div>
          </div>
          <div class="row">
            <div class="left">Originaler DHL Preis</div>
            <div class="right">5,99€</div>
          </div>
          <div class="row">
            <v-btn class="full-width white--text mb-3" color="red"
              >Weiter zum</v-btn
            >
          </div>
        </v-container>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
import ProductRow from "../components/ProductRow.vue";

export default {
  name: "ShippingLabel",
  components: {
    ProductRow,
  },
};
</script>

<style lang="scss">
.products {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.row {
  display: flex;
  width: 300px;
}

.right {
  margin-left: auto;
  font-weight: bold;
}

.full-width {
  width: 100%;
}
</style>
