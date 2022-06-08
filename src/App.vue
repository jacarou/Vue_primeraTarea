<template>
  <div class="">
    <h1 class="texto-rojo">{{ nombre }}</h1>
    <h2 :class="clasePruebas" v-text="codigo"></h2>
    <p v-html="textoHtml"></p>
    <input class="input-grande" type="text" v-model="img" />
    <br />
    <img :src="img" alt="" />
    <br />
    <br />
    <button @click="incrementarContador()">botoncito {{ contador }}</button>
    <br />
    <input type="text" @keyup="presionarTecla()" v-model="inputEvento" />
    <br />

    <select @change="cambiarColor" v-model="colorContenedor">
      <option value="contenedor azul">azul</option>
      <option value="contenedor rojo">rojo</option>
      <option value="contenedor amarillo">amarillo</option>
    </select>

    <div :class="contenedor"></div>
    <br /><br /><br />
    <form @submit="enviarFormulario">
    <input type="text" v-model="inputForm" />  
      <textarea  cols="30" rows="10" v-model="inputForm"></textarea>
      <!-- <input type="submit" value="Enviar" /> -->
    </form>
    <br />
    <p>{{ parrafo }}</p>
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
      img: "https://picsum.photos/800/50",
      clasePruebas: "texto-azul",
      contador: 0,
      inputEvento: "",
      contenedor: "contenedor verde",
      colorContenedor: "contenedor azul",
      inputForm: "",
      parrafo: "",
    };
  },
  methods: {
    incrementarContador() {
      this.contador++;
    },
    presionarTecla() {
      alert(this.inputEvento);
    },
    cambiarColor() {
      this.contenedor = this.colorContenedor;
    },
    enviarFormulario() {
      this.parrafo = this.inputForm;
    },
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
.contenedor {
  width: 100px;
  height: 100px;
}
.verde {
  background-color: green;
}
.azul {
  background-color: blue;
}
.rojo {
  background-color: red;
}
.amarillo {
  background-color: yellow;
}
</style>
