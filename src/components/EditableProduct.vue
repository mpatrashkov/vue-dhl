<template>
  <div class="full-width">
    <v-card>
      <div class="pa-2">
        <div class="d-flex">
          <v-card-title> 5 kg - Paket </v-card-title>
          <div class="d-flex ml-auto ma-3">
            <v-icon large>mdi-pencil-circle</v-icon>
            <v-icon large>mdi-heart-circle</v-icon>
            <v-icon large>mdi-delete-circle</v-icon>
          </div>
        </div>

        <div>
          <ul class="mx-3">
            <li>
              <div class="d-flex justify-space-between">
                <div>30x Paket bis 5kg - Deutschland</div>
                <div>120€</div>
              </div>
            </li>
            <li>
              <div class="d-flex justify-space-between">
                <div>30x Paket bis 5kg - Deutschland</div>
                <div>120€</div>
              </div>
            </li>
            <li>
              <div class="d-flex justify-space-between">
                <div>
                  <!-- Just for spacing -->
                </div>
                <div class="text-h6 font-weight-bold">240€</div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "EditableProduct",
};
</script>

<style lang="scss" scoped>
ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

.full-width {
  width: 100%;
}
</style>
