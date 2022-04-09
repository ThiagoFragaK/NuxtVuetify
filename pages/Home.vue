<template>
  <v-container class="dark lighten-5">
    <v-row>
      <v-col cols="12" sm="12">
        <v-card class="pa-11" outlined tile >
          <h1 class="font-weight-black text-center">Main</h1>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" sm="4" >
        <v-card class="pa-16 text-center" outlined tile >
          Graph#01
        </v-card>
      </v-col>
      <v-col cols="12" sm="4" >
        <v-card class="pa-16 text-center" outlined tile >
          Graph#02
        </v-card>
      </v-col>
      <v-col cols="12" sm="4" >
        <v-card class="pa-16 text-center" outlined tile >
          Graph#03
        </v-card>
      </v-col>
    </v-row>    
  </v-container>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {}
  }
}
</script>
