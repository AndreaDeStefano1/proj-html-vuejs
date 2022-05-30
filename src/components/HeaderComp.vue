<template>
  <header class="d-flex flex-column">

    <NavbarComp class=" pt-4"/>
    <div class="container flex-grow-1 d-flex flex-column justify-content-center text-light position-relative">
      <h1 class="title-font">Barber Shop</h1>
      <div class="divider my-3"></div>
      <span class="mt-2">
        The Pinnacle of Male Grooming
      </span>
      <ButtonComp
      class="mt-3" 
      buttonText="LEARN MORE"/>
      <div class="hero-img position-absolute">
        <img src="../assets/img/avadabarbers_hero_focalmirror-400x550.png" alt="">
      </div>
    </div>

  </header>
</template>

<script>
import NavbarComp from './NavbarComp.vue';
import ButtonComp from './ButtonComp.vue';
export default {
  name: 'HeaderComp',
  components:{
    NavbarComp,
    ButtonComp
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

header{
  background-image: url(../assets/img/avadabarbers-homepage-hero-bg.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 700px;
  h1{
    font-size: 70px;
    font-weight: 800;
  }
  .divider{
    height: 4px;
    width: 190px;
    background-color: $primary-color;
  }
  .hero-img{
    right: 5%;
  }
}
</style>