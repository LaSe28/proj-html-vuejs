<template>
<div>
<div class="background"></div>
<header class="p-relative">
  <div class="nav">
    <img src="../assets/img/theme_eduprime_logo.png" alt="">
    <div class="menu-text">
      <ul>
        <li class="dropdown-parent ml-1 mr-1" v-for="(ele, index) in navMenu" :key="index">
          {{ele.name}} <span v-if="ele.dropdown === true"><i @click="ele.dropdown===true? ele.clicked = true : ''" class="fa-solid fa-chevron-down"></i></span>
          <div :class="ele.clicked === true ? 'show' : '' " class="dropdown">
            <ul>
              <li>opzione1 --------------</li>
              <li>opzione2 --------------</li>
              <li @click="ele.dropdown===true? ele.clicked = false : ''" >opzione3 --------------</li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
    <button class="btn btn-y">VIEW COURSES</button>
  </div>
  <MainSec1/>
</header>
</div>
</template>

<script>
import MainSec1 from './ProjMain1.vue'

export default {
  name: 'HeaderSec',
  components: {
    MainSec1
  },
  data () {
    return {
      i: 0,
      navMenu: [
        {
          name: 'Home',
          dropdown: true,
          clicked: false
        },
        {
          name: 'Courses',
          dropdown: true,
          clicked: false
        },
        {
          name: 'About Us',
          dropdown: false,
          clicked: false
        },
        {
          name: 'News',
          dropdown: true,
          clicked: false
        },
        {
          name: 'Pages',
          dropdown: true,
          clicked: false
        },
        {
          name: 'Contact',
          dropdown: false,
          clicked: false
        },
        {
          name: 'Purchase',
          dropdown: false,
          clicked: false
        }
      ]
    }
  }

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

header{
  background-color: $main-red-tras;
  color: white;
}
.background{
  background: url(../assets/img/theme_slider2_bg-1.jpg);
  height: 60%;
  width: 100%;
  position: absolute;
  top: 0;
  z-index: 0;
}
.nav{
  display: flex;
  align-items: center;
  img{
    height: 100px;
    margin-right: auto;
  }
  ul{
    list-style: none;
    display: flex;
  }
  .menu-text{
    display: flex;
  }
}
.dropdown-parent{
  position: relative;
}
.dropdown{
  position: absolute;
  left: -3rem;
  width: 250px;
  background-color: white;
  color: $main-red;
  display: none;
  ul{
    display: flex;
    flex-direction: column;
  }
  li{
    padding: 1rem;
    margin: .3rem;
  }
  li:hover{
    cursor: pointer;
    background-color: $main-red;
    color: white;
  }
}
.show{
  display: block;
}
.close-menu{
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  bottom: -.5rem;
  right: -.5rem;
  background-color: white;
  height: 20px;
  width: 20px;
  border-radius: 50%;
  padding: 0.5rem;
}

</style>
