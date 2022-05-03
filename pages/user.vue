<template>
  <v-container class="dark lighten-5">
    <v-row>
      <v-col cols="12" sm="12">
        <v-card class="pa-11" outlined tile>
          <h1 class="font-weight-black text-center">{{ user.personaname }}</h1>
          <hr />
          <br />
          <v-card-text>
            <v-row align="center" justify="space-around">
              <v-btn text disabled>Steam Id: {{ user.steamid }}</v-btn>
              <v-btn text disabled>Real Name: {{ user.realname }}</v-btn>
            </v-row>
          </v-card-text>
          <v-card-actions>
            <v-row align="center" justify="space-around">
              <v-btn text to="">Steam Profile</v-btn>
            </v-row>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row dense>
        <v-col v-for="(item, i) in items" :key="i" cols="12">
            <v-card :color="item.color" dark outlined tile>
                <h1 class="font-weight-black text-center">{{ user.personaname }}</h1>
                <hr />
                <div class="d-flex flex-no-wrap justify-space-between">
                    <div>
                        <v-card-title class="text-h5" v-text="item.title" ></v-card-title>

                        <v-card-subtitle v-text="item.artist"></v-card-subtitle>
                        
                        <v-card-actions>
                            <v-btn class="ml-2 mt-5" :href="item.profileUrl" outlined rounded small>
                                Steam Profile
                            </v-btn>
                        </v-card-actions>
                    </div>
                    <v-avatar class="ma-3" size="125" tile>
                        <v-img :src="item.src"></v-img>
                    </v-avatar>
                </div>
            </v-card>
        </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
    data: () => ({
        user: {
        },
      items: [
        {
          color: '#1F7087',
          src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
          title: 'Supermodel',
          artist: 'Foster the People',
        },
        {
          color: '#33415C',
          profileUrl: 'https://steamcommunity.com/id/thiagofragak/',
          src: 'https://steamcdn-a.akamaihd.net/steamcommunity/public/images/avatars/9c/9c9bf21e256237d2dd0d35f07953330b68196cf6_medium.jpg',
          title: 'T.K.',
          artist: 'A Happy Slice of German Bread',
        },
      ],
    }),
    async asyncData({ params, $axios }) {
        const user = await $axios.$get("http://127.0.0.1:9000/api/v1/user");
        console.log(user);
        return { user };
    },
};
</script>

<style>
</style>