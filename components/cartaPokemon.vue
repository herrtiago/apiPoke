<template>
  <div class="carta">
      <img id="imgPokemon" src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/shiny/2.png"  />
      <h5 id="nombrePokemon">
        NOMBRE POKEMON
      </h5>
  </div>
</template>
  
  <style>
.carta{
  display: flex;
  justify-content: center;
  align-items: center;
  background: red;
  border: 4px solid white;
  color:white;
  box-shadow: 0px 10px 15px black;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
}

img{
    height: 100%;
    width: auto;
}
</style>