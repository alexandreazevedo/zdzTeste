<template>
  <v-card>
    <v-toolbar color="white" flat mb-4>

      <v-btn icon light>
        <v-icon color="grey darken-2">mdi-arrow-left</v-icon>
      </v-btn>

      <v-toolbar-title class="grey--text text--darken-4">
        Consulta
      </v-toolbar-title>

      <v-spacer></v-spacer>

    </v-toolbar>
      
    <v-table >

      <thead>
        <tr>
          <th class="text-left">Placa</th>
          <th class="text-left">Hora/Data</th>
          <th class="text-left">Marca/Modelo/Cor</th>
          <th class="text-left">Pagamento</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="item in desserts" :key="item.name">
          <td>{{ item.placa }}</td>
          <td>{{ item.horaData }}</td>
          <td>{{ item.marcaModeloCor }}</td>
        </tr>
      </tbody>

    </v-table>
  </v-card>
</template>


<script>
export default {
  data() {
    return {
      desserts: [
        {
          placa: 'KGJ2A33',
          horaData: '12:45 12/03/2024',
          marcaModeloCor: 'GM Celta 2002',
          pagamento:''
        },
        {
          placa: 'DFG3D22',
          horaData: '12:45 12/03/2024',
          marcaModeloCor: 'GM Celta 2002',
          pagamento:''
        },

      ],
    }
  },
}
</script>