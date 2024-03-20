<template>
  <v-card>
    <v-toolbar color="white" flat>

      <v-btn icon light>
        <v-icon color="grey darken-2">mdi-arrow-left</v-icon>
      </v-btn>

      <v-toolbar-title class="grey--text text--darken-4">
        Cadastro
      </v-toolbar-title>

      <v-spacer></v-spacer>

    </v-toolbar>

    <v-container fluid>
      
      <v-form v-model="valid">

        <v-text-field 
          v-model="estacionamento.placa" :counter="7" :rules="nameRules" label="Placa" required>
        </v-text-field>

        <v-text-field 
          v-model="estacionamento.dataHora" label="Data/Hora" required>
        </v-text-field>

        <v-text-field 
          v-model="estacionamento.marcaModeloCor" label="Marca/Modelo/Cor" required>
        </v-text-field>

        <v-btn :disabled='!valid' color='success' class='mr-4' @click='submit'>
          Salvar
        </v-btn>

        <pre>
          {{ estacionamento }}
        </pre>

      </v-form>
    </v-container>
  </v-card>
</template>



<script>
export default {
  data: () => ({
    valid: true,

    estacionamento: {
      placa: '',
      dataHora: '',
      marcaModeloCor: '',
    },

    nameRules: [
      value => {
        if (value) return true

        return 'A placa é obirgatória.'
      },
      value => {
        if (value?.length == 7) return true

        return 'Deve conter 7 caracteres.'
      },
    ],
  }),

  methods: {
    submit() {
      this.$refs.form.submit()
    },
  },

}

</script>
