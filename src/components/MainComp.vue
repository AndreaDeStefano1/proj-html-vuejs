<template>
  <main>
    <!-- INTRO SECTION -->
    <section class="intro-section pt-5">
      <TitleComp 
      class="mt-5"
      bigText="Pro Barbers"
      miniText="AWARD WINNING"/>
      <ButtonComp 
      class="text-center pb-x"
      buttonText="MEET YOUR NEW BARBER"/>
      
    </section>
    <!-- /INTRO SECTION -->

    <!-- SERVICE SECTION -->
    <section>
      <TitleComp 
      class="mt-5"
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
    </section>
    <!-- /SERVICE SECTION -->
  </main>
</template>

<script>
import ButtonComp from './ButtonComp.vue'
import TitleComp from './TitleComp.vue'
import CardCompServices from './CardCompServices.vue'

export default {
  components: { 
    TitleComp, 
    ButtonComp, 
    CardCompServices },
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
  background-position: 0 20%;
  clip-path: $clip;
    
  .pb-x{
    padding-bottom: 300px;
  }
}

</style>