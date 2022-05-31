<template>
  <footer class="">
    <!-- /footer top -->
    <div class=" d-flex container py-5 justify-content-between">


      <div class="footer-cta  py-5">
        <img class="" src="../assets/img/avadabarbers_footer_shop_image-400x312.png" alt="">
        <ButtonComp
        class="text-center pt-3"
        buttonText="SHOP OUR RANGE NOW"/>
      </div>


      <div class="footer-info d-flex flex-column  py-5">
        <img src="../assets/img/avadabarbers-logo-x2-200x70.png" alt="">
        <p class="text-center pt-5">
         Avada Barbers<br>123New York Street<br>New York City<br>info@yourwewbsite.com<br>+1 (555) 555-1212
        </p>
        <h3 class="text-center pt-5">FOLLOW US</h3>

        <ul class="d-flex justify-content-around pt-3">
          <li class="text-light">
            <i class="fa-brands fa-facebook-square"></i>
          </li>
          <li class="text-light">
            <i class="fa-brands fa-twitter"></i>
          </li>
          <li class="text-light">
            <i class="fa-brands fa-youtube"></i>
          </li>
          <li class="text-light">
            <i class="fa-brands fa-instagram"></i>
          </li>

        </ul>


      </div>


      <div class="footer-cta  py-5">
        <img src="../assets/img/avadabarbers_footer_appointment_image-400x312.png" alt="">
        <ButtonComp
        class="text-center pt-3"
        buttonText="SHOP OUR RANGE NOW"/>
      </div>


    </div>
    <!-- /footer top -->
    <!-- footer bottom -->
    <div class="footer-bottom text-light">
      <p class="text-center">&copy; Copyright 2012-2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by Boolean</p>
    </div>


  </footer>
</template>

<script>
import ButtonComp from './ButtonComp.vue'

export default {
  name: 'FooterComp',
  components:{
    ButtonComp
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

footer{
  width: 100%;
  background-color: $dark-block-color;
  h3{
    color: $primary-color;
  }
  ul{
    list-style: none;
    padding: 0;
    li{
      i{
        font-size: 30px;
      }
    }
  }
  .footer-info p{
  color: gray;

  }
  .footer-bottom{
    height: 100px;
    background-color: lighten($dark-block-color, 3%);
    
    p{
      line-height: 100px;
      color: gray;
    }
  }
}
</style>