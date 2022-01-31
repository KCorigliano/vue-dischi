<template>
    <div class="main">
        <div class="container">
            <discs-container 
                v-for="(disc, index) in discs" 
                :disc="disc"
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
    }
}
</script>

<style lang="scss" scoped>
.main{

    .container{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
    }
}
</style>