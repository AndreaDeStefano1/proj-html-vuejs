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

        <CardCompServices v-for="(service, index) in serviceCardsArray" :key="`card${index}`"
        :text="service.text"
        :title="service.title"
        :url="service.url"/>
        <!-- <CardCompServices 
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
        :url="require('../assets/img/avadabarbers-beardtrim-icon.png')"/> -->

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
      <section class="featured-product-container d-flex">
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
      </section>
     <!-- /FEATURED PRODUCT -->

     <!-- REVIEWES -->
     <section class="reviews-section">

      <TitleComp
        class=" pb-2 text-center" 
        bigText="Reviews"
        miniText="WHAT PEOPLE SAY "/>

        <div class="container d-flex justify-content-center pb-5">

          <CardCompReviews v-for="(review, index) in reviewsArray" :key="`review${index}`"
          class=" flex-column-reverse "
          :text="review.text"
          :title="review.author"
          :url="review.url"/>


        </div>        

     </section>
     <!-- /REVIEWES -->

     <!-- BLOG -->
     <section class="blog-section ">

      <TitleComp
      class=" pt-5 pb-2 text-center" 
      bigText="Recent Blog Posts"
      miniText="TALES FROM THE BARBER SHOP"/>

      <div class="container d-flex">
         
        <CardBlogComp
        class="pt-5"
        v-for="(blog,index) in blogPostArray" :key="`blog${index}`"
        :postImageUrl="blog.url"
        :postText="blog.text"
        :postTitle="blog.title"/>

      </div>

      <ButtonComp
      class="text-center pb-5"
      buttonText="READ MORE FROM OUR BLOG"/>

     </section>


  </main>
</template>

<script>
import ButtonComp from './ButtonComp.vue'
import TitleComp from './TitleComp.vue'
import CardCompServices from './CardCompServices.vue'
import CardCompReviews from './CardCompReviews.vue'
import CardProductComp from './CardProductComp.vue'
import CardBlogComp from './CardBlogComp.vue'


export default {
  components: {
    TitleComp,
    ButtonComp,
    CardCompServices,
    CardProductComp,
    CardCompReviews,
    CardBlogComp
},
  name: 'MainComp',
  data(){
    return{
      serviceCardsArray: [
        {
          text: "Avada Barbers are experts in the lickety split trim and air cut. Quick but careful and ridiculously good looking.",
          title: "Trim & Cut",
          url: require("../assets/img/avadabarbers-trimcut-icon-before.png")
        },
        {
          text: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion.",
          title: "Wash & Dry",
          url: require("../assets/img/avadabarbers-washndry-icon.png")
        },
        {
          text: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.",
          title: "Beard Tidy",
          url: require("../assets/img/avadabarbers-beardtrim-icon.png")
        }
      ],
      blogPostArray: [
        {
          title: 'Avada Barbers Now Open',
          text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Autem mollitia assumenda aspernatur maiores quo.',
          url: require('../assets/img/avadabarbers-second-blog-700x441.jpg')
        },
        {
          title: 'Choosing The Right Barber',
          text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Autem mollitia assumenda aspernatur maiores quo.',
          url: require('../assets/img/avadabarbers-choosing-blog-700x441.jpg')
        },
        {
          title: 'Quick Service Guide',
          text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Autem mollitia assumenda aspernatur maiores quo.',
          url: require('../assets/img/avadabarbers-ourservice-blog-700x441.jpg')
        },
      ],
      reviewsArray: [
        {
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa molestias veritatis corporis laudantium? Cupiditate, voluptatibus aspernatur asperiores quas, laboriosam repellendus mollitia vitae obcaecati sapiente tempore labore. Vitae in nam aut?',
          author: 'Jhon Doe',
          url: require('../assets/img/avadabarbers-trimcut-gallery6-400x400.jpg')
        },
        {
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa molestias veritatis corporis laudantium? Cupiditate, voluptatibus aspernatur asperiores quas, laboriosam repellendus mollitia vitae obcaecati sapiente tempore labore. Vitae in nam aut?',
          author: 'Pete Jones',
          url: require('../assets/img/avadabarbers-trimcut-gallery7-400x402.jpg')
        },
        {
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa molestias veritatis corporis laudantium? Cupiditate, voluptatibus aspernatur asperiores quas, laboriosam repellendus mollitia vitae obcaecati sapiente tempore labore. Vitae in nam aut?',
          author: 'Mark Wilson',
          url: require('../assets/img/avadabarbers-trimcut-gallery3-400x402.jpg')
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';


.intro-section{  
  background-image: url(../assets/img/avadabarbers-about-introbackground.jpg);
  // background-position: 0 10%;
  clip-path: polygon(100% 0, 100% 100%, 50% 90%, 0 100%, 0 0); 
  background-size: 700px 700px;
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

.blog-section{
  clip-path: polygon(50% 20%, 100% 0, 100% 100%, 0 100%, 0 0);
  background-color: #f5f5f5;
  padding-top: 150px;
}
</style>