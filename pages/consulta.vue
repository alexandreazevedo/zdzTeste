<template>
  <v-card>
    <v-toolbar color="white" flat>

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
          <td class="text-left">
            Name
          </td>
          <td class="text-left">
            Hora/Data
          </td>
          <th class="text-left">
            Marca/Modelo/Cor
          </th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="item in desserts" :key="item.name">
          <td>{{ item.name }}</td>
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
          name: 'Frozen Yogurt',
          horaData: '12:45 12/03/2024',
          marcaModeloCor: 'GM Celta 2002'
        },
        {
          name: 'Ice cream sandwich',
          horaData: '12:45 12/03/2024',
          marcaModeloCor: 'GM Celta 2002'
        },

      ],
    }
  },
}
</script>