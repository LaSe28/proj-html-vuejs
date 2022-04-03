<template>
<div style="overflow-x: hidden;" class="p-relative">
  <img style="position: absolute; top:-5px; right: -2rem; width: 105%"  src="../assets/svg/svg-1.svg" alt="">
  <div class="pt-10 container">
    <h2>Last Courses</h2>
    <div class="pb-5 courses-container">
      <div class="course p-relative" v-for="(ele, index) in arrCourses" :key="index" >
        <img :src="ele.icon" :alt="ele.course">
        <h4 style="margin: 0.3rem">{{ele.course}}</h4>
        <div style="margin: 0.3rem">Teacher: <strong>{{ele.teacher}}</strong></div>
        <div style="margin: 0.3rem">Price: <strong>{{ele.price}}</strong></div>
        <button class="btn btn-r">{{ele.textBtn}}</button>
      </div>
    </div>
    <div class="desc-container">
      <div class="desc-text">
        <img style="width: 50px;" src="../assets/img/Exam-icon.png" alt="">
        <h2 class="mb-2">The most efficient examination method</h2>
        <p class="mb-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit. At ipsam minima culpa obcaecati officia incidunt nisi voluptatibus consequuntur adipisci placeat nemo ab libero voluptatum, corrupti, debitis quo distinctio reprehenderit velit?</p>
        <button class="btn btn-r">Discover the Method</button>
      </div>
      <div class="desc-img">
        <img src="../assets/img/Exam-Illustration.png" alt="">
      </div>
    </div>
    <div class="desc-container">
      <div class="desc-img">
        <img src="../assets/img/Girl-Illustration.png" alt="">
      </div>
      <div class="desc-text pb-5">
        <img style="width: 50px;" src="../assets/img/Exam-icon-1.png" alt="">
        <h2 class="mb-2">Variable fees for international students</h2>
        <p class="mb-2">Lorem, ipsum dolor sit amet consectetur adipisicing elit. At ipsam minima culpa obcaecati officia incidunt nisi voluptatibus consequuntur adipisci placeat nemo ab libero voluptatum, corrupti, debitis quo distinctio reprehenderit velit?</p>
        <button class="btn btn-r">List of Fees</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import img1 from '../assets/img/Decisions-icon.png'
import img2 from '../assets/img/Speaker-icon.png'
import img3 from '../assets/img/Network-icon.png'
import img4 from '../assets/img/Brand-icon.png'

export default {
  name: 'MainSec4',
  data () {
    return {
      arrCourses: [
        {
          course: 'Make Better Decisions',
          teacher: 'James Colins',
          price: '$21.00',
          icon: img1,
          textBtn: 'View Course'
        },
        {
          course: 'How to be a speaker',
          teacher: 'James Colins',
          price: 'Free',
          icon: img2,
          textBtn: 'View Course'
        },
        {
          course: 'Network Introductios',
          teacher: 'James Colins',
          price: 'Free',
          icon: img3,
          textBtn: 'View Course'
        },
        {
          course: 'Brand Management',
          teacher: 'James Colins',
          price: 'Free',
          icon: img4,
          textBtn: 'View Course'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';
h2{
  font-size: 2.4rem;
}
.courses-container{
  display: flex;
  justify-content: space-between;
}
.course{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 4rem 1rem;
  height: 220px;
  width: 220px;
  box-shadow: 0 1px 6px #ececee;
  img{
    width: 70px;
  }
  .btn{
    padding: .7rem 1rem;
    position: absolute;
    bottom:-1.3rem;
  }
}
.desc-container{
  display: flex;
  .desc-img{
    img{
      width: 100%;
      padding: 3rem;
    }
  }
  .desc-text{
    color: $text-blue;
    width: 80%;
  }
}

</style>
