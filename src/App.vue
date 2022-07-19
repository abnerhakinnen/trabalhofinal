<template>

    <TheHeader/>
    <main id="main">
        <router-view/>
        <LivrosLista/>
    </main>
    
    
    <TheFooter/>

</template>

<script>
import TheFooter from "./components/TheFooter.vue";
import TheHeader from "./components/TheHeader.vue";
import LivrosLista from "./components/LivrosLista.vue";


export default {
  components: {
    TheFooter,
    TheHeader,
    LivrosLista
  }
};
</script>

<style>

</style>
