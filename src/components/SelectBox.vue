<template>
    <div class="container">
        <select v-model="genreList">
            <option value="">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
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
select{
    background-color: #2e3a46;
    color: white;
    margin-bottom: 30px;
    border: none;
    padding: 5px 15px;
    cursor: pointer;
}
</style>