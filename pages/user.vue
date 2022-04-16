<template>
    <v-container class="dark lighten-5">
        <v-row>
            <v-col cols="12" sm="12">
            <v-card class="pa-11" outlined tile >
                <h1 class="font-weight-black text-center">Main</h1>
                {{ user }}
            </v-card>
            </v-col>
        </v-row>    
    </v-container>  
</template>

<script>
export default {
    async asyncData({ params, $axios }) {
        const user = await $axios.$get('http://127.0.0.1:8000/api/user');
        return { user }
    }
}
</script>

<style>

</style>