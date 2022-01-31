<template>
    <div class="navbar">
        <img src="@/assets/Spotify_logo_without_text.svg" alt="">
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.navbar{
    height: 75px;
    width: 100%;
    background-color: #2e3a46;
    padding: 0 15px;

    img{
        height: calc(100% - 30px);
        margin: 15px 0;
    }
}
</style>