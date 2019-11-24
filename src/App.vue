<template>
  <v-app>
    <v-content>
      <CardView />
    </v-content>
  </v-app>
</template>

<script>
import CardView from './views/CardView'

export default {
  name: 'App',

  components: {
    CardView
  },

  data: () => ({
    //
  })
}
</script>
