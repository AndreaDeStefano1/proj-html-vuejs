<template>
  <div class="card-container d-flex flex-column">

    <div class="img-&-title d-flex flex-column ">

      <div class="image-container text-center">
        <img  :src="url" alt="">
      </div>
      
      <h4 class=" text-center">{{title}}</h4>

    </div>

    <div class="description">
      <p class="text-center pt-3">
        {{text}}
      </p>
    </div>

  </div>
</template>

<script>
export default {
  name: 'CardCompServices',
  props:{
    url: String,
    title: String,
    text: String
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';



.card-container{
  // border: 1px solid red; 
  margin: 10px;
  .image-container{
    height: 250px;  
    img{
      width: 150px;
      height: 219px;      
    }
  }
  h4{
    color: $primary-color
  }
}
</style>