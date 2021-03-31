<template>
  <v-card>
    <div class="vertical-container">
      <div class="header bold my-2">
        <div class="price">7,90€</div>
        <div class="information">i</div>
      </div>
      <div class="title">5 kg - Paket</div>
      <div class="description my-3">
        <ul>
          <li>Sendungsnumer</li>
          <li>Etikett zum drucken</li>
        </ul>
      </div>
      <v-btn class="mx-auto white--text mb-3" color="red">Wahlen</v-btn>
    </div>
  </v-card>
</template>

<script>
export default {
  name: "Product",
};
</script>

<style lang="scss" scoped>
.header {
  background-color: orange;
  width: 100%;
  padding: 15px;
  text-align: center;
  font-weight: bolder;
  position: relative;
}

.information {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translate(-50%, 50%);
  border-radius: 50%;
  border: 2px solid black;
  width: 25px;
  height: 25px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  cursor: pointer;
}

.vertical-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
