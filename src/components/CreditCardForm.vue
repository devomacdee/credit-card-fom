<template>
  <v-app id="inspire">
    <v-content>
      <v-container
        class="fill-height"
        fluid
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col
            cols="12"
            sm="8"
            md="5"
          >
            <v-card class="elevation-12">
              <v-card-text>
                <v-form>
                  <v-text-field
                    v-model="cardNumber"
                    label="Card number"
                    name="card-number"
                    type="text"
                  />

                  <v-text-field
                    id="cardholder"
                    v-model="cardHolder"
                    label="Card holder"
                    name="cardholder"
                    type="text"
                  />

                  <div class="expiry">
                    <v-select
                      id="expiry-month"
                      v-model="month"
                      label="month"
                      :items="months"
                    />
                    <!-- <v-spacer /> -->
                    <v-select
                      id="expiry-year"
                      v-model="year"
                      label="year"
                      :items="years"
                    />
                    <!-- <v-spacer /> -->
                    <v-text-field
                      label="CSV"
                      name="csv"
                      type="text"
                    />
                  </div>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn
                  color="primary"
                  :block="true"
                >
                  Submit
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'CreditCardForm',
  props: {
    source: String
  },
  computed: {
    months () {
      let months = []
      for (let i = 1; i < 13; i++) {
        const month = '0' + i.toString()
        months.push(month.slice(-2))
      }
      return months
    },
    years () {
      let year = new Date().getFullYear()
      const limit = year + 10
      let years = []
      while (year < limit) {
        years.push(year)
        year++
      }
      return years
    }
  },
  data () {
    return {
      month: '',
      year: '',
      cardHolder: '',
      csv: ''
    }
  }
}
</script>
<style lang="scss" scoped>
  .expiry {
    display: flex;
    justify-content: space-between;

    .v-input {
      max-width: 29%;
    }
  }
</style>
