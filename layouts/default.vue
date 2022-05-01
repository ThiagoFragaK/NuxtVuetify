<template>
  <v-app dark>

     <v-app-bar :clipped-left="clipped" fixed app>
      <v-spacer />
      <v-btn icon to="/">
          <v-icon>mdi-home</v-icon>
        </v-btn>

        <v-btn icon to="user">
          <v-icon>mdi-account-outline</v-icon>
        </v-btn>

        <v-btn icon to="games">
          <v-icon>mdi-bookmark-outline</v-icon>
        </v-btn>

        <v-btn icon >
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-app-bar>

    <!-- Body -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Kalkulator'
    }
  }
}
</script>
