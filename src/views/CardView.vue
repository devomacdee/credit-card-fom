<template>
  <v-app>
    <v-content>
      <div class="card-container">
        <Card />
        <CardForm />
      </div>
    </v-content>
  </v-app>
</template>

<script>
import CardForm from '../components/CardForm'
import Card from '../components/Card'

export default {
  name: 'CardView',

  components: {
    CardForm,
    Card
  },

  data: () => ({
    //
  })
}
</script>
<style lang="scss" scoped>
.card-container {
  position: relative;
}
</style>
