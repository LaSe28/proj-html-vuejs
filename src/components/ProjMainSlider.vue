<template>
<div>
  <div class="container">
    <div class=" mt-2 centered">
      <h2>Faculties Available at EduPrime</h2>
      <p>A single university with a load of courses, tailored to satisfy any student's needs.</p>
    </div>
  </div>
  <div class="slider-container mt-2 mb-2">
    <div @click="i = index" :class="i === index ? 'active': '' " class="slider-ele mt-1" v-for="(ele, index) in courses" :key="index">
      <img :src="ele.imgSmall" alt="ele.name">
      <p class="mt-1 " >{{ele.name}}</p>
    </div>
  </div>
  <div class="container">
    <div class="centered-row">
      <img class="mr-2" :src="courses[i].img" alt="">
      <div class="ml-2">
        <h3 class="mb-2 ">{{courses[i].name}}</h3>
        <p>{{courses[i].text}}</p>
        <button class="mt-2 btn btn-r">Read More</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import img1 from '../assets/img/Gavel-v2.png'
import img2 from '../assets/img/Coins-tabs-v2.png'
import img3 from '../assets/img/Medicine-tabs-v2.png'
import img4 from '../assets/img/Computer-tabs-v2.png'
import img5 from '../assets/img/Palette-tabs-v2.png'
import img6 from '../assets/img/Gavel-Illustration-e1556884768193.png'
import img7 from '../assets/img/Economy.png'
import img8 from '../assets/img/Medicine.png'
import img9 from '../assets/img/Computer-Science.png'
import img10 from '../assets/img/Graphic-Design.png'
export default {
  name: 'SliderSec',
  data () {
    return {
      i: 0,
      courses: [
        {
          name: 'Law Faculty',
          imgSmall: img1,
          img: img6,
          text: 'testo numero 1 Learning from world-leading academics and practitioners, you\'ll not only receive an outstanding '
        },
        {
          name: 'Economy',
          imgSmall: img2,
          img: img7,
          text: 'testo numero 2 Learning from world-leading academics and practitioners, you\'ll not only receive an outstanding '
        },
        {
          name: 'Medicine',
          imgSmall: img3,
          img: img8,
          text: 'testo numero 3 Learning from world-leading academics and practitioners, you\'ll not only receive an outstanding '
        },
        {
          name: 'Computer science',
          imgSmall: img4,
          img: img9,
          text: 'testo numero 4 Learning from world-leading academics and practitioners, you\'ll not only receive an outstanding '
        },
        {
          name: 'Graphic Design',
          imgSmall: img5,
          img: img10,
          text: 'testo numero 5 Learning from world-leading academics and practitioners, you\'ll not only receive an outstanding '
        }
      ]
    }
  }

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_general.scss';
h2{
  font-size: 2.4rem;
}
h3{
  font-size: 2rem;
}
.slider-container{
  display: flex;
  justify-content: center;
}
.slider-ele{
  color: $main-red;
  font-weight: bold;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1px solid black;
  width: 200px;
  height: 180px;
  img{
    width: 60%;
  }
}

.active{
  position: relative;
  background-color: $main-red;
  color: white;
  img{
    filter: brightness(250%);
  }
}
.active::before{
  content: '';
  height: 20px;
  width: 20px;
  background-color: $main-red;
  position: absolute;
  bottom: -10px;
  transform: rotate(45deg);
  z-index: 0;
}
</style>
