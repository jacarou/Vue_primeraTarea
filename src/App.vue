<template>
  <div class="">
    <h1 class="texto-rojo">{{ nombre }}</h1>
    <h2 :class="clasePruebas" v-text="codigo"></h2>
    <p v-html="textoHtml"></p>
    <input class="input-grande" type="text" v-model="img" />
    <br />
    <img :src="img" alt="" />
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      nombre: "Jhony Alejandro Caro Umbariba",
      codigo: "20191020055",
      textoHtml: "<h1>Texto probando el v-html.</h1>",
      img: "https://picsum.photos/500/200",
      clasePruebas: "texto-azul",
    };
  },
};
</script>
<style>
.texto-azul {
  color: blue;
}
.texto-rojo {
  color: red;
  background-color: black;
}
.input-grande {
  width: 20%;
  height: 25px;
  margin: 5px;
}
</style>
