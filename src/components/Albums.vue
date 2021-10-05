<template>
    <div class="container">
        <Album :key="index" v-for="(album, index) in filterAlbums" :info="album"/>
    </div>
</template>

<script>
import axios from 'axios'
import Album from './Album.vue'

export default {
    name: 'Albums',
    components: {
        Album
    },
    props: ["filt"],
    data() {
        return {
            albums: []
        }
    },
    created() {
        axios
            .get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( (resp) => {
                this.albums = resp.data.response;
        })
    },
    computed: {
        filterAlbums() {
            if (this.filt === "All" || this.filt === "") {
                return this.albums
            } else {
                return this.albums.filter(
                (item) => item.genre === this.filt
            );
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/common.scss';

    .container {
        width: 70%;
        margin: 70px auto;
        display: flex;
        flex-wrap: wrap;
    }

</style>