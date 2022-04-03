<template>
<div class="main-container">
  <div class="container">
    <div class="centered">
      <h2 class="m-2">Partners</h2>
      <p class="mb-2">Leverage agile frameworks to provide a robust synopsis for high level overviews. iterative approaches to corporate strategy.</p>
      <div class="partners">
        <div v-for="(ele, index) in arrParters" :key="index" class="partner">
          <img :src="ele" alt="">
        </div>
      </div>
    </div>
  </div>
  <div style="background-color: #f7f8fa; height: 200px; overflow: hidden;" class="p-relative">
    <img class="background" src="../assets/img/background-wave3.png" alt="">
  </div>
</div>
</template>

<script>
import img1 from '../assets/img/partner-1.png'
import img2 from '../assets/img/partner-2.png'
import img3 from '../assets/img/partner-3.png'
import img4 from '../assets/img/partner-4.png'
import img5 from '../assets/img/partner-5.png'
import img6 from '../assets/img/partner-6.png'
import img7 from '../assets/img/partner-7.png'
import img8 from '../assets/img/partner-8.png'

export default {
  name: 'PartnersSec',
  data () {
    return {
      arrParters: [
        img2,
        img3,
        img4,
        img5,
        img6,
        img8,
        img1,
        img7
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

.container{
  position: relative;
  z-index: 10;
  color: $text-blue;
  h2{
    font-size: 2.4rem;
  }
}
.partners{
  display: flex;
  .partner{
    img{
      height: 40px;
      margin: 1rem;
      opacity: .5;
      &:hover{
        opacity: 1;
      }
    }
  }
}
.background{
  height: 230%;
  width: 130%;
  position: absolute;
  top: 0;
}

</style>
