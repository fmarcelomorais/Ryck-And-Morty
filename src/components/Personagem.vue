<template>
 
        <div class="row">
          <div >
            <div
              class="card col s12"
              v-for="personagem of personagens"
              :key="personagem.id" >
              <div class="card-image">
                <img :src="personagem.image" />
              </div>
              <div class="card-content">
                <table class="striped">
                  <thead>
                    <tr>
                      <th>Nome</th>
                      <th>Gênero</th>
                      <th>Origem</th>
                      <th>Espécie</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>{{personagem.name}}</td>
                      <td>{{personagem.gender}}</td>
                      <td>{{personagem.origin.name}}</td>
                      <td>{{personagem.species}}</td>
                    </tr>
                      </tbody>
                      <thead>
                      <tr>
                        <th>Situação</th>
                        <th>Episodios</th>
                        <th>Localização</th>
                        <th>Tipo</th>  
                      </tr>
                      </thead>
                      <tbody>
                      <tr>
                      <td>{{personagem.status}}</td>
                      <td>{{personagem.episode.length}}</td>
                      <td>{{personagem.location.name}}</td>
                      <td>{{personagem.type}}</td>
                    </tr>
                  </tbody>
                </table>               
              </div>              
            </div>
          </div>
        </div>
       
  </template>

<script>
import personagens from '../service/personagens'

export default { 
  data() {
    return {
      personagens: [],
    };
  },
mounted() {
    personagens.listar().then((resposta) => {
      this.personagens = resposta.data.results;
      return this.personagens;
    });
  },
}

</script>

<style scoped>




</style>>

