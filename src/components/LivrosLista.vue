<template>
    <section class="livros-container">
            <br>
            <h1 class="title">Biblioteca</h1>
            <div class="livro" v-for="livro in livros" :key="livro.id">
            <router-link to="/livros/id" class="livros">
            <p class="titulo">Título: {{livro.title}}</p>
            <br>
            <p>Autor: {{livro.publisher}}
            <br>
            Avaliação: {{livro.rating}}
            </p>
            </router-link>
            </div>
    </section>
</template>

<script>
export default{
    data(){
        return{
            livros: null,
        };
    },
    methods: {
        getLivros(){
            fetch("http://localhost:1337/api/books?populate=cover")
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
.livros-container{
    max-width: 1000px;
    margin: 0 auto;
}

.livros{
display:grid;
grid-template-columns: repeat(3, 1fr);
grid-gap: 30px;
margin: 30px;
text-decoration: none;
color: orange;
}

.livros:hover{
    color: black;
        box-shadow: 0 6px 12px rgba(30, 60, 90, 0.2);
        transform: scale(1.1);

}
.livros{
    box-shadow: 0 4px 8px rgba(30, 60, 90, 0.1);
    padding: 10px;
    background: #fff;
    border-radius: 4px;
    transition: all 0.2s;
}

.title{
    color:orange;
    text-align: center;
}

.title:hover{
    color:black;
}
</style>