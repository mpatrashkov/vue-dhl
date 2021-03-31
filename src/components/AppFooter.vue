<template>
  <v-container>
    <footer class="footer">
      <div class="column">
        <div class="title">Privatkunden</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
      </div>
      <div class="column">
        <div class="title">Privatkunden</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
      </div>
      <div class="column">
        <div class="title">Privatkunden</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
      </div>
      <div class="column">
        <div class="title">Privatkunden</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
        <div>Preise</div>
      </div>
    </footer>
  </v-container>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style lang="scss">
$gap: 10px;

.footer {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}

.column {
  display: flex;
  flex-direction: column;
  margin: -$gap 0;
}

.column > * {
  padding: $gap 0;
}

.title {
  font-weight: bolder;
  font-size: 24px;
}
</style>
