<template>
    <div class="card">
        <div class="info">
            <img :src="info.poster">
            <h2>{{info.title}}</h2>
            <h4>{{info.author}}</h4>
            <h5>{{info.year}}</h5>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Album',
    props: ['info']
}
</script>

<style lang="scss" scoped>
    @import '../style/common.scss';

    .card {
        width: calc(100% / 5 - 20px);
        height: 330px;
        background-color: $headerBg;
        margin: 10px;
        margin-bottom: 20px;
        text-align: center;
            .info {
                padding: 17.5px 10px;
                img {
                    width: 90%;
                    min-height: 150px;
                    margin-bottom: 15px;
                }
                h2 {
                    color: #fff;
                    margin-bottom: 30px;
                    font-size: 1.3rem;
                }
                h4, h5 {
                    color: #55626e;
                }
            }
            
    }
</style>