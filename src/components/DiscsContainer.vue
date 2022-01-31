<template>
    <div class="disc-container">
        <div>
            <img :src="disc.poster" alt="">
        </div>
        <p>{{disc.title}}</p>
        <p>{{disc.author}}</p>
        <p>{{disc.year}}</p>
        
    </div>
</template>

<script>
export default {
    props: {
        disc: Object
    }
}
</script>

<style lang="scss" scoped>
.disc-container{
    width: calc((100% / 5) - 30px);
    background-color: #2e3a46;
    padding: 15px;

    img{
        width: 100%;
    }
}
</style>