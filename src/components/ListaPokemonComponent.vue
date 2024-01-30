<template>
    <div>
        <h1>Listado de pokemon</h1>
        <BuscadorPokemonComponent></BuscadorPokemonComponent>

        <div>
            <!-- <div v-for="(pokemon, index) in pokemons" :key="index">

                {{ pokemon  }} -->

                <PokemonCardComponent :data="pokemons"></PokemonCardComponent>
                
                
                
            <!-- </div> -->
            
        </div>
        
    </div>
</template>

<script>

import BuscadorPokemonComponent from './BuscadorPokemonComponent.vue';
import PokemonCardComponent from './PokemonCardComponent.vue';

import axios from "axios";


export default {
    name: 'PokedexListaPokemon',

    data() {
        return {
            pokemons: []
            
        };
    },
    components: {
        BuscadorPokemonComponent,
        PokemonCardComponent
    },


    mounted () {

    },
    created(){

        this.getPokemons();
        
    },

    methods: {

        async getPokemons(){
            //  await axios.get('https://pokeapi.co/api/v2/pokemon?limit=100000&offset=0').then(
             await axios.get('https://pokeapi.co/api/v2/pokemon').then(
                data => {

                    const { data : { results } } = data 
                    
                    results.map(pokemon => {
                        pokemon.id = pokemon.url.split('/').filter(function(part){
                            return !!part}).pop();
                        this.pokemons.push(pokemon)
                    });

                }
            );
            
        }
        
    },
};
</script>

<style scoped>


</style>