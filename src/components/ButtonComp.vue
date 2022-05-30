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
  border-width: 3px;
  padding: 10px 25px;
  & > span{
    color: $primary-color ;
    font-weight: 500;
  }
}

.btn-outline-secondary:hover {
    /* color: #fff; */
  background-color: transparent; 
  border-color: darken($primary-color, 10%) ; 

  & > span{
  color: darken($primary-color, 10%);  
  }
}


button:focus:not(:focus-visible) {
  box-shadow: none;
}

</style>