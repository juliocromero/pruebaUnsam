<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="18" md="10">
     <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"

  
       
    

    :value="value"
    color grow="indigo"
  >
    <template v-slot:header.name="{ header }">
      {{ header.text.toUpperCase() }}
    </template>
  </v-data-table>
     <v-bottom-navigation
    :value="value"
    color="indigo"
    grow
  >
    <v-btn>
      <span>SOLEADO</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>VENTOSO</span>
       <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn>
      <span>NUBLADO</span>

      <v-icon>mdi-fire</v-icon>
    </v-btn>

    <v-btn>
      <span>LLUVIOSO</span>
      <v-icon>mdi-water</v-icon>
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
        { text: 'lunes', value: 'name' }, //columnas
        { text: 'martes', value: 'fat' },
        { text: 'miercoles', value: 'carbs' },
        { text: 'jueves', value: 'protein' },
        { text: 'viernes', value: 'iron' },
        { text: 'sabado' , value: '.'}
      ],
      desserts: [
        {
          name: 'julio',
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {name: 'agosto',
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%', },
        {
          name: 'septiembre',
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',
        },    

      { name: 'octubre',
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',},
      ],
    }),
}
</script>
