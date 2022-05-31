<template>
  <div class="mx-2 pb-5">
    <div class="image-container">
      <img :src="postImageUrl" alt="">
    </div>
    <h2 class="text-center py-3">{{postTitle}}</h2>
    <p class="text-center">{{postText}}</p>
  </div>
</template>

<script>
export default {
  name: 'CardBlogComp',
  props:{
    postTitle: String,
    postText: String,
    postImageUrl: String
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

  div{
    width: calc(100% / 3);
    .image-container{
      width: 100%;
      img{
        width: 100%
      };
    }
    h2{
      font-family: $title-font;
      color: $primary-color;
    }
  }
</style>