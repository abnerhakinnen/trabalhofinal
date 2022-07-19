<template>
<h1 class="title">Biblioteca</h1>
</template>

<script>
export default{
    data(){
        return{
            id: null,
        };
    },
    methods: {
        getLivros(){
            fetch("http://localhost:1337/api/books/id")
            .then(response => response.json())
            .then(response => {
                this.livros = response.data;
            })
        },
    },

    created(){
        this.getLivros();
    }
};
</script>

<style scoped>

</style>