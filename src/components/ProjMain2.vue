<template>
<div class="p-relative">
  <img class="background" src="../assets/img/home-background.png" alt="">
  <div class="container pb-10 flex">
    <div class="text">
      <img src="../assets/img/Books-icon.png" alt="">
      <h2 class="mb-2">Thousands of courses for any type of student</h2>
      <p class="mb-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Magni fugit aspernatur minus ad, dolor et ratione reiciendis unde, necessitatibus quis ab tempora. Debitis dicta beatae obcaecati quis saepe? Aliquid, provident.</p>
      <button class="btn btn-y">Browse through courses</button>
    </div>
    <img class="m-2" src="../assets/img/Graduation-Illustration.png" alt="">
  </div>
</div>
</template>

<script>
export default {
  name: 'MainSec2'

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_general.scss';
.flex{
  display: flex;
  img{
    width: 400px;
  }
}
.background{
  position: absolute;
  z-index: -1;
  top: 0 ;
  height: 100%;
  width: 100%;
  filter: grayscale(50%);
  background: url(../assets/img/home-background.png);
}
.text{
  color: $text-blue;
  h2{
    font-size: 2.4rem;
    font-weight: bold;
  }
  img{
    width: 50px;
  }
}

</style>
