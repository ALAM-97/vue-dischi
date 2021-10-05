<template>
    <header>
        <img src="../assets/spotify-logo.png" alt="">
        <select v-model="genre" @change="$emit('filter', genre)" placeholder="Seleziona un genere...">
            <option selected value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            genre: ""
        }
    }
}

</script>

<style lang="scss" scoped>
    @import '../style/common.scss';
    
        header {
            background-color: $headerBg;
            display: flex;
            justify-content: space-between;
            align-items: center;
            img {
                width: 5%;
                padding: 10px 0;
            }
            select {
                width: 200px;
                height: 30px;
                border-radius: 5px;
                margin-right: 20px;
            }
        }
</style>