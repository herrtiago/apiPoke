<template>
  <nuxt-link class="flex" :to="nombre">
    <div class="carta">
      <img id="imgPokemon" :src="url" />
      <h5 id="nombrePokemon">{{ nombre }}</h5>
    </div>
  </nuxt-link>
</template>
  
<script>
export default {
  name: "CartaPokemon",
  props: {
    nombre: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
};
</script>




    <style>
.carta {
  display: flex;
  justify-content: center;
  align-items: center;
  background: red;
  border: 4px solid white;
  color: white;
  box-shadow: 0px 10px 20px black;
  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: center;
  height: 50vh;
  width: 22vw;
}

img {
  height: 85%;
}
.carta {
  color: #fff;
  background: linear-gradient(45deg, red, blue, green, black);
  background-size: 400% 400%;
  position: relative;
  animation: cambiar 10s ease-in-out infinite;
}

@keyframes cambiar{
			0%{background-position: 0 50%;}
			50%{background-position: 100% 50%;}
			100%{background-position: 0 50%;}
		}
</style>