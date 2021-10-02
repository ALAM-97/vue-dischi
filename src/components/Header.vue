<template>
    <header>
        <img src="../assets/spotify-logo.png" alt="">
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
    @import '../style/common.scss';
    
        header {
            background-color: $headerBg;
            img {
                width: 5%;
                padding: 10px 0;
            }
        }
</style>