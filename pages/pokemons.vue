<template>
  <div class="main">
    <div class="titulo">
      <h1>PokeDEx</h1>
    </div>
    <div class="buscador">
      <input type="text" placeholder="Buscar pokemon" />
    </div>
    <div class="cartas">
        <cartaPokemon /> <cartaPokemon /> <cartaPokemon /> <cartaPokemon />
      <cartaPokemon /> <cartaPokemon />  <cartaPokemon /> <cartaPokemon /> <cartaPokemon /> <cartaPokemon />
      <cartaPokemon /> <cartaPokemon />
    </div>
  </div>
</template>


<script>
export default {
  name: "pokemonsPage",
};
</script>

<style>
html {
  height: 100%;
}
.main {
  background-color: aquamarine;
  height: 100%;
}

.

.cartas {
width: 100%;
height: 100%;
padding: 1rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 1rem;
}


::-webkit-scrollbar{
    display: none;
}
</style>