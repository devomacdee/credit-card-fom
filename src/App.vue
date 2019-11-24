<template>
  <v-app>
    <v-content>
      <CreditCardForm />
    </v-content>
  </v-app>
</template>

<script>
import CreditCardForm from './components/CreditCardForm'

export default {
  name: 'App',

  components: {
    CreditCardForm
  },

  data: () => ({
    //
  })
}
</script>
