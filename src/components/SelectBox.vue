<template>
    <div class="container-fluid">
        <div class="container">
            <select v-model="genreList" @change="$emit('selectArray', genreList)">
                <option value="">All</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            genreList: '',
        }
    },
}
</script>

<style lang="scss" scoped>
.container-fluid{
    width: 100%;
    background-color: #1e2d3b;

    .container{
        width: 1200px;
        margin: 0 auto;
        display: flex;

        select{
            background-color: #2e3a46;
            color: white;
            margin-bottom: 30px;
            border: none;
            padding: 5px 15px;
            cursor: pointer;
            margin: 30px 0 0 15px;
        }
    }
}

</style>