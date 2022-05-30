<template>
  <main>
    <!-- INTRO SECTION -->
    <section class="intro-section pt-5">
      <TitleComp 
      class=" text-center"
      bigText="Pro Barbers"
      miniText="AWARD WINNING"/>
      <ButtonComp 
      class="text-center pb-x mt-5"
      buttonText="MEET YOUR NEW BARBER"/>
      
    </section>
    <!-- /INTRO SECTION -->

    <!-- SERVICE SECTION -->
    <section>
      <TitleComp 
      class="mt-5 text-center"
      bigText="Services"
      miniText="MENS GROOMING"/>
      <div class="container d-flex justify-content-center">

        <!-- <CardComp v-for="(service, index) in serviceCardsArray" :key="`card${index}`"
        :text="service.text"
        :title="service.title"
        :url="service.url"/> -->
        <CardCompServices 
        text="Avada Barbers are experts in the lickety split trim and air cut. Quick but careful and ridiculously good looking."
        title="Trim & Cut"
        :url="require('../assets/img/avadabarbers-trimcut-icon-before.png')"/>
        <CardCompServices 
        text="Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion."
        title="Wash & Dry"
        :url="require('../assets/img/avadabarbers-washndry-icon.png')"/>
        <CardCompServices 
        text="Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers."
        title="Beard Tidy"
        :url="require('../assets/img/avadabarbers-beardtrim-icon.png')"/>

      </div>

      <ButtonComp 
      class="text-center pt-3"
      buttonText="READ ABOUT OUR SERVICES"/>

    </section>
    <!-- /SERVICE SECTION -->

    <!-- PRODUCT SECTION -->
    <section class="product-section mt-5">
      <TitleComp 
      class=" text-center"
      bigText="Avada Grooming Product"
      miniText="WE HAVE YOU COVERED"/>
      <div class="produc-container d-flex justify-content-center py-5 ">
        <CardProductComp
        price="18.91"
        title="Brush"
        :url="require('../assets/img/brush_dark.png')"/>
        <CardProductComp
        price="85.00"
        title="Scissors"
        :url="require('../assets/img/scissors.png')"/>
        <CardProductComp
        price="15.00"
        title="Hot Oil"
        :url="require('../assets/img/hot_oil_dark.png')"/>
        <CardProductComp
        price="30.00"
        title="Straight Razor"
        :url="require('../assets/img/straight_razor_dark.png')"/>

      </div>
      <ButtonComp 
      class="text-center pt-3 pb-x"
      buttonText="READ ABOUT OUR SERVICES"/>


    </section>

     <!-- /PRODUCT SECTION -->
      <div class="featured-product-container d-flex">
        <div class="image-container">
          <img src="../assets/img/shaving_butter.png" alt="">
        </div>
        <div class="text-field">
          <TitleComp
          class=" pb-2 " 
          bigText="Shaving Butter"
          miniText="THIS MONTH FEATURED PRODUCT"/>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illo, suscipit ratione minima quis soluta, veritatis neque aliquam numquam architecto vitae totam optio voluptatem accusamus laboriosam?</p>
          <ButtonComp
          buttonText="BUY NOW"/>
        </div>
      </div>
     <!-- /FEATURED PRODUCT -->

  </main>
</template>

<script>
import ButtonComp from './ButtonComp.vue'
import TitleComp from './TitleComp.vue'
import CardCompServices from './CardCompServices.vue'
import CardProductComp from './CardProductComp.vue'


export default {
  components: {
    TitleComp,
    ButtonComp,
    CardCompServices,
    CardProductComp
},
  name: 'MainComp',
  data(){
    return{
      serviceCardsArray :[
        {
          text: "Avada Barbers are experts in the lickety split trim and air cut. Quick but careful and ridiculously good looking.",
          title: "Trim & Cut",
          url: "../assets/img/avadabarbers-trimcut-icon-before.png"
        },
        {
          text: "Avada Barbers are experts in the lickety split trim and air cut. Quick but careful and ridiculously good looking.",
          title: "Trim & Cut",
          url: "../assets/img/avadabarbers-trimcut-icon-before.png"
        },
        {
          text: "Avada Barbers are experts in the lickety split trim and air cut. Quick but careful and ridiculously good looking.",
          title: "Trim & Cut",
          url: "../assets/img/avadabarbers-trimcut-icon-before.png"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';



.intro-section{  
  background-image: url(../assets/img/avadabarbers-about-introbackground.jpg);
  background-position: 0 25%;
  clip-path: polygon(100% 0, 100% 100%, 50% 90%, 0 100%, 0 0); 
  .pb-x{
    padding-bottom: 150px;
  }
}
.product-section{
  background-image: url(../assets/img/avadabarbers-reviewsbackground.jpg);
  // min-height: 600px;
  background-size: cover;
  background-position: bottom;
  clip-path: polygon(50% 0%, 100% 10%, 100% 100%, 0 100%, 0 10%);
  padding-top: 150px;
  .pb-x{
    padding-bottom: 120px;
  }
}


.featured-product-container{
  width: 60%;
  height: 300px;
  background-color: $dark-block-color;
  border-color: 1px solid red;
  transform: translateY(-60px);
  margin: 0 auto;
  border-top: 4px solid $primary-color;
  .image-container{
    width: 300px;
    height: 296px;
    background-image: url(../assets/img/avadabarbers-cta-background.jpg);
    background-position: center;
    background-size: cover;
    img{
      width: 240px;
      margin: 40px 40px;
    }
  }
  .text-field{
    padding: 20px;
    h6{
      color: $primary-color;
    }
    h2{
      color: $secondary-color;
      font-size: 3em;
    }
  }
}


</style>