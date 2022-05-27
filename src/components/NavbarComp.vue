<template>
  <div class=" container">

    <nav class=" d-flex justify-content-between align-content-center">

      <div class="logo ">
        <img src="../assets/img/avadabarbers-logo-x1.png" alt="">
      </div>

      <div class="menu d-flex ">
        <div class="shop">
          <font-awesome-icon icon="fa-solid fa-cart-shopping" />
        </div>
        <div class="menu-collapsed">
          <font-awesome-icon icon="fa-solid fa-bars" />
        </div>
      </div>

    </nav>

  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.menu{
  padding: 5px;


  .shop,
  .menu-collapsed{
    color: white;
    padding: 10px;
    font-size: 1.4em;
  }
}
</style>