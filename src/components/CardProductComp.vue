<template>
  <div class="card-container d-flex flex-column">
    <img class=" text-center" :src="url" alt="">
		<h3 class=" text-center">{{title}}</h3>
		<span class=" text-center">${{price}}</span>
	</div>
</template>

<script>
export default {
    name: "CArdProductComp",
    props:{
        url: String,
        title: String,
        price: String
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
h3,
span{
	color: $primary-color
}
img{
	width: 300px;
}
</style>