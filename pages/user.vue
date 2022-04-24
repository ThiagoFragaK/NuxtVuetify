<template>
    <v-container class="dark lighten-5">
        <v-row>
            <v-col cols="12" sm="12">
            <v-card class="pa-11" outlined tile >
                <h1 class="font-weight-black text-center">Main</h1>
                {{ user.personaname }}
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
    }
}
</script>

<style>

</style>