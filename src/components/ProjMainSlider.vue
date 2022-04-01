<template>
<div class="container">
  <div>Faculties Available at EduPrime</div>
  <p>A single university with a load of courses, tailored to satisfy any student's needs.</p>
  <div v-for="(ele, index) in courses" :key="index">
    <img :src="ele.imgSmall" alt="ele.name">
    <p>{{ele.name}}</p>
  </div>

</div>
</template>

<script>
import img1 from '../assets/img/Gavel-v2.png'
import img2 from '../assets/img/Coins-tabs-v2.png'
import img3 from '../assets/img/Medicine-tabs-v2.png'
import img4 from '../assets/img/Computer-tabs-v2.png'
import img5 from '../assets/img/Palette-tabs-v2.png'
export default {
  name: 'SliderSec',
  data () {
    return {
      courses: [
        {
          name: 'Law Faculty',
          imgSmall: img1
        },
        {
          name: 'Economy',
          imgSmall: img2
        },
        {
          name: 'Medicine',
          imgSmall: img3
        },
        {
          name: 'Computer science',
          imgSmall: img4
        },
        {
          name: 'Graphic Design',
          imgSmall: img5
        }
      ]
    }
  }

}
</script>

<style scoped lang="scss">
.container{
  display: flex;
  flex-wrap: wrap;
}
</style>
