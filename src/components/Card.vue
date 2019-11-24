<template>
<v-container>
  <v-row
    align="center"
    justify="center"
  >
    <div class="card-item">
      <h1 class="card-type">Credit Card</h1>
    </div>
  </v-row>
</v-container>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.card-item {
  position: absolute;
  width: 350px;
  height: 200px;
  border: 1px solid black;
  border-radius: 4px;
  top: 20%;
  z-index: 100;
  background-color: white;
  padding: 8px;

  .card-type {
    font-size: 1.5rem;
  }
}
</style>
