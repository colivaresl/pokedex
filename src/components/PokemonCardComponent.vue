<template>
    <div>
      <!-- <h1 v-text="data.descriptions"></h1> -->

      <div class="list p-2">

        <div v-for="(pokemon, index) in data" :key="index">
          <div class="card">
            <h4><b v-text="pokemon.name.charAt(0).toUpperCase() + pokemon.name.slice(1)"></b></h4> 
            
            <img :src="imageUrl+ pokemon.id+'.png'">
            <h4 v-text="'N°'+pokemon.id"></h4>

          </div>
        </div>


      </div>

    </div>
</template>

<script>
export default {
    name: 'PokedexPokemonCardComponent',

    props: ['data'],

    data() { 
        return {
          imageUrl: "https://raw.githubusercontent.com/pokeapi/sprites/master/sprites/pokemon/",

            
        };
    },

    mounted() {
        
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

.list{
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  grid-gap: 10px;
  width: 150%;
  max-width: 100%;
}
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  height: 300px;
  /*
  width: 10%;

  */
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

.container {
  padding: 2px 16px;
}

</style>