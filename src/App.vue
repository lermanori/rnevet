<template>
  <v-app id="inspire" dark>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      fixed
      app
    >
      <v-list dense>
        <v-list-tile to="/">
          <v-list-tile-action>
            <v-icon>home</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Home</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to="/about">
          <v-list-tile-action>
            <v-icon>help_outline</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>About</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Application</v-toolbar-title>
    </v-toolbar>
    <v-content style="z-index:1">
           <transition name="page-transition" mode="out-in" appear enter-active-class="animated fadeInLeft"  leave-active-class="animated fadeOutRight">
            <router-view/>
           </transition>
    </v-content>
      <app-background/>
    <v-footer app fixed>
      
    </v-footer>
  </v-app>
</template>

<script>
import Background from "./components/Background"

  export default {
    data: () => ({
      drawer: null
    }),
    props: {
      source: String
    },
    components:{
      'app-background':Background
    }
  }
</script>