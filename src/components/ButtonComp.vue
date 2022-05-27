<template>
  <div>
    <button class="btn btn-outline-secondary">
      <span>{{buttonText}}</span>
    </button>
  </div>  
</template>

<script>
export default {
  name: 'ButtonComp',
  props:{
    buttonText: String
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';


button{
  border-radius: 0;
  border-color: $primary-color;
  padding: 10px 25px;
  & > span{
    color: $primary-color ;
    font-weight: 500;
  }
}
</style>