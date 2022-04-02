<template>
<div style="overflow-x: hidden;" class="p-relative">
  <img style="position: absolute; top:-5px; right: -2rem; width: 105%"  src="../assets/svg/svg-1.svg" alt="">
  <div class="pt-10 container">
    <h2>Last Courses</h2>
    <div class="courses-container">
      <div class="course" v-for="(ele, index) in arrCourses" :key="index" >
        <img :src="ele.icon" :alt="ele.course">
        <h4>{{ele.course}}</h4>
        <div>Teacher: <strong>{{ele.teacher}}</strong></div>
        <div>Price: <strong>{{ele.price}}</strong></div>
        <button class="btn btn-r">{{ele.textBtn}}</button>
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
          textBtn: 'Viev Course'
        },
        {
          course: 'How to be a speaker',
          teacher: 'James Colins',
          price: 'Free',
          icon: img2,
          textBtn: 'Viev Course'
        },
        {
          course: 'Network Introductios',
          teacher: 'James Colins',
          price: 'Free',
          icon: img3,
          textBtn: 'Viev Course'
        },
        {
          course: 'Brand Management',
          teacher: 'James Colins',
          price: 'Free',
          icon: img4,
          textBtn: 'Viev Course'
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
  margin-top: 4rem;
  img{
    width: 80px;
  }
  .btn{
    padding: .7rem 1rem;
  }
}

</style>
