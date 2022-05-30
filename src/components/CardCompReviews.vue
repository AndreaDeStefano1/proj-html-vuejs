<template>
  <div class="card-container d-flex flex-column flex-column-reverse mx-5 px-2">

    <div class="img-&-title d-flex flex-column ">

      <div class="image-container text-center mt-1">
        <img class=" img-fluid " :src="url" alt="">
      </div>
      
      <h5 class=" text-center">{{title}}</h5>

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
  //border: 1px solid red; 
  margin: 10px;
  width: 300px;
  .image-container{
    height: 120px;  
    img{
      width: 100px;
      border-radius: 50%;
    }
  }
  h5{
    color: $primary-color
  }
}
</style>