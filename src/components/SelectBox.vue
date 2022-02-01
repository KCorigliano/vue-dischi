<template>
    <div class="container-fluid">
        <div class="container">
            <select v-model="genreList" @change="genreFilter">
                <option value="">All genre</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>

            <select v-model="authorList" @change="authorFilter">
                <option value="">All author</option>
                <option value="Bon Jovi">Bon Jovi</option>
                <option value="Queen">Queen</option>
                <option value="Sting">Sting</option>
                <option value="Steve Gadd Band">Steve Gadd Band</option>
                <option value="Iron Maiden">Iron Maiden</option>
                <option value="Eric Clapton">Eric Clapton</option>
                <option value="Deep Purple">Deep Purple</option>
                <option value="Metallica">Metallica</option>
                <option value="Dave Weckl">Dave Weckl</option>
                <option value="Michael Jacjson">Michael Jackson</option>
            </select>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            genreList: '',
            authorList: '',
        }
    },
    methods: {
        genreFilter (){
            this.authorList = '',
            this.$emit('selectArray', this.genreList)
        },
        authorFilter (){
            this.genreList = '',
            this.$emit('authorArray', this.authorList)
        }
    },
}
</script>

<style lang="scss" scoped>
.container-fluid{
    width: 100%;

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