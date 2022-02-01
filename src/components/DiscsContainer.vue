<template>
    <div class="disc-container">
        <div>
            <img :src="disc.poster" alt="">
        </div>
        <h2>{{disc.title}}</h2>
        <p>{{disc.author}}</p>
        <p>{{disc.year}}</p>
        
    </div>
</template>

<script>
export default {
    props: {
        disc: Object,
    },
}
</script>

<style lang="scss" scoped>
.disc-container{
    width: calc((100% / 5) - 30px);
    background-color: #2e3a46;
    margin: 0 15px;
    padding: 20px;
    margin-bottom: 30px;
    text-align: center;
    color: grey;

    img{
        width: 100%;
    }

    h2{
        color: white;
        margin: 15px 0;
    }
}
</style>