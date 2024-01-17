<template>
  <div id="app">
    <img alt="Pokedex logo" src="./assets/pokedex_logo.png">

    <lista-pokemon></lista-pokemon>
  </div>
</template>

<script>
import ListaPokemon from './components/ListaPokemonComponent.vue';

export default {
  name: 'App',
  components: {
    ListaPokemon
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
