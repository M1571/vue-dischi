// ------------------------------------
// HTML

<template>
    
    <ul class="album-wrapper">
        <!-- COMPONENTE CARD -->
        <Album class="albummss" v-for="(album,i) in albums" :key="i" :album="album"></Album>

    </ul>

</template>

// ------------------------------------
// JS

<script>

import axios from 'axios'
import Album from './AlbumCard.vue'

    export default {
        components: {
            Album,
        },
        data() {
            return {
                albums: []
            }
        },
        methods: {
            fetchAlbums: function() {

                // CHIAMO SERVER CON API: https://flynn.boolean.careers/exercises/api/array/music
                axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then( res => {
                    this.albums = res.data.response
                })
                .catch( err => {
                    console.error( err.response)
                })
                // SALVO ARRAY CON ALBUM DENTRO this.album
            }
        },
        // INSTALLO AXIOS
        created() {
            this.fetchAlbums()
        }
    }
</script>

// ------------------------------------
// CSS

<style lang="scss" scoped>

.album-wrapper {
    display: flex;
    flex-wrap: wrap;
    gap: 25px calc( 10% / 4 );
}

.albummss {
    width: 18%;
}

</style>