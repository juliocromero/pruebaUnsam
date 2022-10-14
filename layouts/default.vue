<template>
  <v-app dark>
    <!-- desde aca arranca el navbar -->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!-- aca termina el navbar -->
    <!-- aca comienza el siderbar -->
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      color="#5d95c9"
    >
      <v-app-bar-nav-icon color="white" @click.stop="drawer = !drawer" />
      <v-spacer />
      <div>
      <!-- aca el icono de usuario -->
      <InputSelect />
    </div>
    
    </v-app-bar>
    
    <!-- aca termina el siderbar -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    
  </v-app>
</template>

<script>
import 'material-design-icons-iconfont/dist/material-design-icons.css'
import InputSelect from '../components/Select/inputSelect.vue';
export default {
    name: "DefaultLayout",
    data() {
        return {
            clipped: true,
            drawer: true,
            fixed: true,
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/"
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire"
                },
                {
                    icon: "home_work",
                    title: "home",
                    to: "/home"
                },
            ],
            miniVariant: false,
            right: false,
            rightDrawer: false,
            title: "Vuetify.js"
        };
    },
    components: { InputSelect }
}
</script>
