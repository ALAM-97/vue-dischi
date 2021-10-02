<template>
    <div class="container">
        <Album :key="index" v-for="(album, index) in albums" :info="album"/>
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
}
</script>

<style lang="scss" scoped>
    @import '../style/common.scss';

    .container {
        width: 70%;
        margin: 70px auto;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

</style>