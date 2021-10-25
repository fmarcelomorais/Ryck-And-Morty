<template>
  <div class="container">
    <Header/>
    <Personagem/>
  </div>   
</template>

<script>
import Header from './components/Header.vue'
import Personagem from './components/Personagem.vue'
export default {
    components: {
      Header,
      Personagem,
  },
 
};
</script>

<style scoped>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css";
</style>
