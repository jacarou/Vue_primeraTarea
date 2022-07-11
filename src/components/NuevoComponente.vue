<template>
  <div class="card">
    <h1>{{ titulo }}</h1>
    <div class="contenedor-img">
      <img :src="imagen" />
    </div>
    <p class="parrafo">{{ descripcion }}</p>
  </div>
</template>

<script>
export default {
  props: {
    titulo: "",
    imagen: "",
    descripcion: "",
  },
};
</script>

<style>
.card {
  background-color: rgba(128, 128, 128, 0.603);
  padding: 10px;
  margin: 5px;
  width: 30%;
  border-radius: 25px;
  box-shadow: 5px 5px 5px rgb(75, 75, 75);
}
.contenedor-img {
  width: 100%;
  overflow: hidden;
}
img {
  height: 200px;
  width: 200px;
  object-fit: cover;
  border-radius: 50%;
}
.parrafo {
  text-align: justify;
}
.card:hover {
  background-color: rgba(204, 201, 201, 0.932);
}
</style>
