<template>
    <div class="container">
        {{disc.title}}
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
.container{
    width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
}
</style>