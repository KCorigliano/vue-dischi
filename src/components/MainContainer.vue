<template>
    <div class="main">
        <div class="container">
            <discs-container 
                v-for="(disc, index) in discs" 
                :disc="disc"
                :index="index"
                :key="index"/>   
        </div>
    </div>
</template>

<script>
import DiscsContainer from './DiscsContainer.vue'

export default {
    components: {
        DiscsContainer,
    }, 
    props: {
        discs: Array
    },
}
</script>

<style lang="scss" scoped>
.main{
    padding: 20px;

    .container{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
    }
}
</style>