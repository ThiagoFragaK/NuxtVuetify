<template>
    <v-container class="dark lighten-5">
        <v-row>
            <v-col cols="12" sm="12">
                <v-card class="pa-11" outlined tile >
                    <h1 class="font-weight-black text-center">{{ user.personaname }}</h1>
                    <hr>
                    <br/>
                    <v-row align="center" justify="space-around" >
                        <v-btn text disabled>Steam Id: {{ user.steamid }}</v-btn>
                        <v-btn text disabled>Real Name: {{ user.realname }}</v-btn>
                        <v-btn text to="this.profileUrl()">Steam Profile</v-btn>
                    </v-row>
                </v-card>
            </v-col>
        </v-row>    
    </v-container>  
</template>

<script>
export default {
    async asyncData({ params, $axios }) {
        const user = await $axios.$get('api/v001/user');
        return { user }
    },
    profileUrl(){
        return user.profileurl;
    }
}
</script>

<style>
</style>