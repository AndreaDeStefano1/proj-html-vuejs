<template>
  <div class=" ">
    <h6 class="">{{miniText}}</h6>
    <h2 class="title-font">{{bigText}}</h2>
  </div>
</template>

<script>
export default {
  name: 'TitleComp',
  props:{
    miniText: String,
    bigText: String
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

div{
  h6{
    color: $primary-color;
  }
  h2{
    color: $secondary-color;
    font-size: 3em;
    font-weight: 800;
  }
}

</style>