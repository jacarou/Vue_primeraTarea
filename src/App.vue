<template>
  <div class="contenedor-principal">
    <h1 class="titulo-principal">CARTAS DE CARRITOS</h1>
    <div class="cartas">
      <NuevoComponente
        :titulo="'Lamborghini'"
        :descripcion="lorem"
        :imagen="imagenes[0]"
      />
      <NuevoComponente
        :titulo="'Ferrari'"
        :descripcion="lorem"
        :imagen="imagenes[1]"
      />
      <NuevoComponente
        :titulo="'Maserati'"
        :descripcion="lorem"
        :imagen="imagenes[2]"
      />
      <NuevoComponente
        :titulo="'BMW'"
        :descripcion="lorem"
        :imagen="imagenes[3]"
      />
      <NuevoComponente
        :titulo="'Mercedes Benz'"
        :descripcion="lorem"
        :imagen="imagenes[4]"
      />
      <NuevoComponente
        :titulo="'Audi'"
        :descripcion="lorem"
        :imagen="imagenes[5]"
      />
    </div>
  </div>
</template>
<script>
import NuevoComponente from "./components/NuevoComponente.vue";
// import { watch } from "@vue/runtime-core";
export default {
  name: "App",
  data() {
    return {
      imagenes: [
        "https://www.lamborghini.com/sites/it-en/files/DAM/lamborghini/facelift_2019/models_gw/hero-banner/2022/04_12/gate_models_og_01.jpg",
        "https://phantom-expansion.unidadeditorial.es/9a14c3fda6b79d4f2f58df87b33d61a0/crop/0x725/2043x1875/resize/1200/f/webp/assets/multimedia/imagenes/2022/05/20/16530388017130.jpg",
        "https://www.diariomotor.com/imagenes/2017/07/maserati-01-marca-1536x909.jpg",
        "https://img.remediosdigitales.com/3a9597/bmw-serie-8-coupe_7/1366_2000.jpg",
        "https://autosdeprimera.com/wp-content/uploads/2021/07/mercedes-amg-e-53-4matic-coupe.jpg",
        "https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/styles/1200/public/media/image/2021/03/video-conducir-audi-rs-tron-gt-256-km-h-autobahn-silencio-2256587.jpg?itok=san-w9J_",
      ],
      lorem:
        "Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto dignissimos accusamus, adipisci eveniet error sed dicta laboriosam ex consequuntur explicabo quod temporibus veniam neque sunt asperiores quidem debitis rem qui?",
    };
  },
  methods: {},
  computed: {},
  // watch: {},
  components: { NuevoComponente },
};
</script>
<style>
* {
  font-family: "Lato", sans-serif;
}

body {
  background: rgb(230, 230, 230);
  background-size: cover;
  background-repeat: no-repeat;
}
.contenedor-principal {
  text-align: center;
}
.titulo-principal {
  color: rgb(145, 71, 71);
  text-shadow: 1px 1px 2px black;
  font-weight: 900;
}
.cartas {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around
}
</style>
