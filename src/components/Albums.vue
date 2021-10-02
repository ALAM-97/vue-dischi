<template>
    <div class="container">
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
        <Album/>
    </div>
</template>

<script>
import Album from './Album.vue'

export default {
    name: 'Albums',
    components: {
        Album,
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
        justify-content: space-between;
    }

</style>