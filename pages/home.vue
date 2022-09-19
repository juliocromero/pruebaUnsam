<template>
  <div>
    <v-carousel>
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
          

        ></v-carousel-item>
      </v-carousel>
     
       
      <div>
        <v-btn class="septiembre" fab dark large>
          <v-icon dark>
            add_circle
          </v-icon>
      
        </v-btn>
  
        
        <v-btn class="octubre" fab dark large>
          <v-icon>
            delete
          </v-icon>
        
  
        </v-btn>
      </div>
  </div>
    
</template>



<h1>

</h1>

<script>
    export default {
      data () {
        return {
          items: [
            {
              src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
            },
            {
              src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            },
            {
              src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
            },
            {
              src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
            },
          ],
        }
      },
    }
  </script>
  <style>
.septiembre{
  margin-top: 10px;
    background-color: green !important;
}
.octubre{
  margin-left: 90%;
    background-color: red !important;
}


  </style>