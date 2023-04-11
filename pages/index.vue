<template>
  <div class="main">
    <div class="titulo">
      <h1>PokeDEx</h1>
    </div>
    <div class="buscador">
      <input type="text" placeholder="Buscar pokemon" />
    </div>
    <div class="cartas">
      <carta-pokemon
        v-for="i in response"
        :key="i"
        :nombre="i.name"
        :url="i.sprites.front_default"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      response: [],
    };
  },
  mounted() {
    this.getInfo();
  },
  methods: {
    async getInfo() {
      for (let j = 1; j < 20; j++) {
        const { data } = await this.$axios.get(`pokemon/${j}`);
        this.response.push(data);
      }
    },
  },
};
</script>


<style>
@import url("https://fonts.googleapis.com/css2?family=Delicious+Handrawn&family=Sedgwick+Ave+Display&display=swap");

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
  height: 10vh;
  width: 50%;
  text-align: center;
  font-family: "Delicious Handrawn", cursive;
  font-family: "Sedgwick Ave Display", cursive;
}

.buscador {
  height: 10vh;
  align-self: baseline;
  margin-left: 1%;
  width: 25%;
}

.buscador input {
  padding: 0.5em;
  width: 100%;
  border-radius: 40px;
}
.cartas {
  width: 100%;
  height: 100%;
  padding: 1rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 1rem;
}

::-webkit-scrollbar {
  display: none;
}
</style>