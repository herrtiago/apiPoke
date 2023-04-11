<template>
  <div class="carta">
      <img id="imgPokemon" :src="url"  />
      <h5 id="nombrePokemon">{{ nombre }}
      </h5>
  </div>
</template>
  
<script>
export default{
  name:"CartaPokemon",
  props:{
    nombre:{
      type: String,
      required: true,
    },
    url:{
      type: String,
      required: true,
    }
  }
}
</script>




  <style>
.carta{
  display: flex;
  justify-content: center;
  align-items: center;
  background: red;
  border: 4px solid white;
  color:white;
  box-shadow: 0px 10px 20px black;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  height: 50vh;
}

img{
    height: 85%;
    width: auto;
}
</style>