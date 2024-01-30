<template>
    <div>
        <input type="text" v-model="inputPokemon" placeholder="Buscar Pokemon..." />

        <button 
        type="button" 
        class="btn btn-primary"
        >Buscar</button>
        
        <!-- @click="imprimirPokemonABuscar()" -->
        
    </div>
</template>


<script>

// import { Button } from 'bootstrap';

export default {
    name: 'PokedexBuscadorPokemonComponent',

    data() {
        return {
            inputPokemon: ""
        };
    },
    components: {
        // Button
        

    },

    mounted() {
        
    },

    methods: {
    
        
    },
};
</script>

<style scoped>
input[type=text]{
    border: 1px solid;
    border-radius: 20px;
    
}



</style>