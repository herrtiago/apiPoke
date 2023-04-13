<template>
  <div class="main">
    <div class="titulo">
      <h1>{{ ruta.name }}</h1>
    </div>
    <div class="info">
      <div class=" h-[100%] w-[50%]">
        <h2>Habilidades</h2>
        <p v-for="i in ruta.abilities" :key="i.name">
          {{ i.ability.name }}
        </p>
        <h2>Stats</h2>
        <p v-for="i in ruta.stats" :key="i.stat.name">
          {{ i.stat.name }} : {{ i.base_stat }}
        </p>
        <img class="imgFront" :src="urlImg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PokemonPage",
  data() {
    return {
      ruta: [],
      urlImg: "",
    };
  },
  mounted() {
    this.getInfo();
  },
  methods: {
    async getInfo() {
      const { data } = await this.$axios.get(`pokemon${this.$route.path}`);
      this.ruta = data;
      console.log(this.ruta);
      this.urlImg = this.ruta.sprites.other.dream_world.front_default;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Sedgwick+Ave+Display&display=swap");

body,
html {
  height: 100%;
}
.main {
  background-color: aquamarine;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.titulo {
  font-size: 3rem;
  height: 10%;
  width: 50%;
  text-align: center;
  font-family: "Delicious Handrawn", cursive;
  font-family: "Sedgwick Ave Display", cursive;
}

.info {
  height: 80vh;
  width: 80%;
  background-color: rgb(230, 217, 201);
  display: flex;
  align-content: center;
  justify-content: center;
  color: black;
  border-radius: 40px;
  text-align: center;
}

h2 {
  font-family: "Delicious Handrawn", cursive;
  font-family: "Sedgwick Ave Display", cursive;
  margin-top: 1.5rem;
}

.imgFront {
  height: 40%;
  width:40%;
  margin: auto;
}
</style>