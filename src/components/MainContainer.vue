<template>
    <div class="main">
        <div class="container">
            <discs-container />
        </div>
    </div>
</template>

<script>
import DiscsContainer from './DiscsContainer.vue'

export default {
    components: {
        DiscsContainer,
  }
}
</script>

<style lang="scss" scoped>
.container{
    width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
}
</style>