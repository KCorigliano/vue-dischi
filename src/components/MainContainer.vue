<template>
    <div class="main">
        <div class="container">
            <select-box />
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
import SelectBox from './SelectBox.vue'

export default {
    components: {
        DiscsContainer,
        SelectBox
    }, 
    data() {
        return {
            currentIndex: 0,
        }
    },
    props: {
        discs: Array
    },
    mounted() {
        console.log('questo è il currentIndex: ' + this.currentIndex)
    },
}
</script>

<style lang="scss" scoped>
.main{
    background-color: #1e2d3b;
    padding: 50px;

    .container{
        width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
}
</style>