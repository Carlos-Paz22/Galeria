<template>
         <div class="card">
          <img :src="imagen.url" class="card-img-top"  />
          <div class="card-body">
            <h5 class="card-title">{{ imagen.created_at }}</h5>
          </div>
        </div>
</template>


<script>
export default {
    
    name: 'Imagen',
    props:["imagen"],



}
</script>