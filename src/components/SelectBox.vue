<template>
    <div class="container-fluid">
        <div class="container">
            <select v-model="genreList" @change="genreFilter">
                <option value="">All genre</option>
                <option 
                    v-for="(genre, index) in autoGenreList" 
                    :key="index" 
                    :value="genre"
                >
                    {{genre}}
                </option>
            </select>

            <select v-model="authorList" @change="authorFilter">
                <option value="">All author</option>
                <option 
                    v-for="(author, index) in autoAuthorList" 
                    :key="index" 
                    :value="author"
                >
                    {{author}}
                </option>
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
    props: {
        autoGenreList : Array,
        autoAuthorList : Array,
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