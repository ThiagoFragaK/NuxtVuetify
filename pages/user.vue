<template>
  <v-container class="dark lighten-5">
    <v-row>
      <v-col cols="12" sm="12">
        <v-card class="pa-11" outlined tile>
          <h1 class="font-weight-black text-center">T.K.</h1>
          <hr />
          <br />
          <v-card-text>
            <v-row align="center" justify="space-around">
              <v-btn text disabled>Steam Id: 45653</v-btn>
              <v-btn text disabled>Real Name: Slice of German Bread</v-btn>
            </v-row>
          </v-card-text>
          <br/>
          <v-card-actions>
            <v-row align="center" justify="space-around">
              <v-btn text to="">Steam Profile</v-btn>
            </v-row>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: '#33415C',
        profileUrl: 'https://steamcommunity.com/id/thiagofragak/',
        src: 'https://steamcdn-a.akamaihd.net/steamcommunity/public/images/avatars/9c/9c9bf21e256237d2dd0d35f07953330b68196cf6_medium.jpg',
        title: 'T.K.',
        artist: 'A Happy Slice of German Bread',
      },
    ],
  }),
};
</script>

<style>
</style>