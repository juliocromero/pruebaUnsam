<template>

  <div>
    <v-card class="mx-auto" max-width="344">
      <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" height="200px"></v-img>



      <v-card-title>
        CLIENTE
      </v-card-title>

      <v-card-subtitle>
        soy un cliente
      </v-card-subtitle>

      <v-card-actions>
        <v-btn color="green" text>
          guardar
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}

          </v-icon>
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn color="pink" text>
          cerrar

          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>

          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for
            sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you
            add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to
            escape.
          </v-card-text>
        </div>
      </v-expand-transition>

    </v-card>
    <div class="div">
      <v-btn class="hola" fab dark large>
        <v-icon dark>
          add_circle
        </v-icon>
      </v-btn>

      <v-btn class="dia" fab dark large>
        <v-icon>
          delete
        </v-icon>

      </v-btn>
    </div>

  </div>



</template>


<script>
  import 'material-design-icons-iconfont/dist/material-design-icons.css'
  export default {
    name: 'InspirePage',
    show: false,
    data: () => ({})
  }
  


</script>

<style>
  .hola {
    margin-top: 10px;
    margin-left: -170px;
    background-color: green !important;
  }

  .dia {
    margin-top: 10px;
    margin-left: 210px;
    background-color: red !important;
   

  }
  .div {
    margin-left: 50%;
  }
</style>