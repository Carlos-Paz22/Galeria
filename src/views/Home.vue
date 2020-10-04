<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <h1 class="text-center">Imagenes</h1>
      </div>
    </div>

    <div class="row">
      <div class="col-12 col-sm-6 col-md-4" v-for="imagen in imagenes" :key="imagen.id" >
        <Imagen :imagen="imagen"/>
      </div>
    </div>
  </div>
</template>

<script>

import Imagen  from '../components/Imagen'


export default {

  name: "Home",
  components:{
    Imagen
  },
  data() {
    return {
      imagenes: [],
    };
  },
  mounted() {
    fetch("https://api.jeisontech.dev/api/images/")
      .then((res) => res.json())
      .then((data) => {
        this.imagenes = data;
      });
  },
  /*  beforeCreate(){
    console.log("beforeCreate")
  },
  created(){
    console.log("created")
  },
  beforeMount(){
    console.log("beforeMount")
  },
  mounted(){
    console.log("mounted")
  } */
};
</script>

<style>
</style>
