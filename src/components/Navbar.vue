<template>
    <nav>
        <v-app-bar fixed app>
            <span>
                <v-icon class="grey--text" @click="drawer = !drawer">menu</v-icon>
            </span>
            <v-spacer></v-spacer>
            <v-toolbar-title class="text-uppercase grey--text">
                <span>Orchard</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <span>
                <v-icon>exit_to_app</v-icon>
            </span>
        </v-app-bar>

        <v-navigation-drawer app v-model="drawer" class="green">
            
        </v-navigation-drawer>
    </nav>
</template>
<script>
    export default {
        data() {
            return {
                drawer: false
            }
        },
        name: 'nav-bar'
    }
</script>