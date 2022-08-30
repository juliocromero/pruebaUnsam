<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="18" md="10">
     <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"
  >
    <template v-slot:header.name="{ header }">
      {{ header.text.toUpperCase() }}
    </template>
  </v-data-table>
     <v-bottom-navigation
    :value="value"
    color="teal"
    grow
  >
    <v-btn>
      <span>Recents</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>Favorites</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn>
      <span>Nearby</span>
      <v-icon>mdi-map-marker</v-icon>
    </v-btn>
  </v-bottom-navigation>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data: () => ({
      headers: [
        { text: 'Nombre', value: 'name' }, //columnas
        { text: 'hola', value: 'fat' },
        { text: 'Carbs (g)', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
      ],
      desserts: [
        {
          name: 'julio',
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {
          name: 'juan',
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',
        },      
      ],
    }),
}
</script>
