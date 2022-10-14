<template>
    <v-container fluid>
        <v-row justify="center">
            <v-menu bottom min-width="200px" rounded offset-y>
                <template v-slot:activator="{ on }">
                    <v-btn icon x-large v-on="on">
                        <v-icon color="white">person</v-icon>
                    </v-btn>
                </template>
                <v-card>
                    <v-list-item-content class="justify-center">
                        <div class="mx-auto text-center">
                            
                            <v-btn text>
                                <v-icon>vpn-key</v-icon>
                                Cambiar Contraseña
                            </v-btn>
                            <v-divider></v-divider>
                            <v-btn text>
                                Salir
                            </v-btn>
                        </div>
                    </v-list-item-content>
                </v-card>
            </v-menu>
        </v-row>
    </v-container>

</template>

<script>
import 'material-design-icons-iconfont/dist/material-design-icons.css'
export default {
    data: () => ({
    })
}

</script>