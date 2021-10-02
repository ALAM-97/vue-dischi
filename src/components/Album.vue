<template>
    <div class="card">
        <div class="info">
            <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
            <h2>NEW JERSEY</h2>
            <h4>Bon Jovi</h4>
            <h5>1988</h5>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Album'
}
</script>

<style lang="scss" scoped>
    @import '../style/common.scss';

    .card {
        width: calc(100% / 5 - 20px);
        height: 330px;
        background-color: $headerBg;
        margin-bottom: 20px;
        text-align: center;
            .info {
                padding: 17.5px 10px;
                img {
                width: 90%;
                margin-bottom: 15px;
                }
                h2 {
                    color: #fff;
                    margin-bottom: 30px;
                }
                h4, h5 {
                    color: #55626e;
                }
            }
            
    }
</style>