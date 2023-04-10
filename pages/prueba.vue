<template>
    <div>
        <p>Vista de prueba</p>
        <p >{{ nombre }}
        <img v-if="mostrar" src="/muelle.jpeg" alt=""></p>
        <button @click="cambiar">Cambiar</button>


    </div>
</template>
  
<script>
export default {
    name: 'PruebaPage',
    data() {
        return {
            nombre: "Santiago",
            estadoNombre: true,
            mostrar: true,
        }
    },
    methods: {
        cambiar() {
            if (this.estadoNombre == true) {
                this.nombre = "Herrera Suarez";
                this.estadoNombre = false;
                this.mostrar = false;
            }
            else {

                this.nombre = "Santiago";
                this.estadoNombre = true;
                this.mostrar = true;
            }
        }
    }
}

</script>
  
<style>
button {
    background-color: red;
}

img{
    width: 250px;
    height: 250px;
}
</style>