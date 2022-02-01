<template>
<div class="container">
    <div class="lds-ring">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </div>
</div>

</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.container{
    width: 100%;
    height: 100vh;
    display: flex;
    align-content: center;
    justify-content: center;
    background-color: #1e2d3b;

    .lds-ring {
    display: inline-block;
    position: relative;
    width: 150px;
    height: 150px;
    margin-top: 50vh;
    }
    .lds-ring div {
    box-sizing: border-box;
    display: block;
    position: absolute;
    width: 64px;
    height: 64px;
    margin: 8px;
    border: 8px solid #fff;
    border-radius: 50%;
    animation: lds-ring 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
    border-color: #fff transparent transparent transparent;
    }
    .lds-ring div:nth-child(1) {
    animation-delay: -0.45s;
    }
    .lds-ring div:nth-child(2) {
    animation-delay: -0.3s;
    }
    .lds-ring div:nth-child(3) {
    animation-delay: -0.15s;
    }
    @keyframes lds-ring {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
    }
}

</style>