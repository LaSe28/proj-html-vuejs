<template>
<header>
  <div class="nav">
    <img src="../assets/img/theme_eduprime_logo.png" alt="">
    <div class="menu-text">
      <ul>
        <li v-for="(ele, index) in navMenu" :key="index">{{ele.name}}</li>
      </ul>
    </div>
    <button class="btn btn-y">VIEW COURSES</button>
  </div>
  <MainSec1/>
</header>
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
      navMenu: [
        {
          name: 'Home',
          dropdown: true
        },
        {
          name: 'Courses',
          dropdown: true
        },
        {
          name: 'About Us',
          dropdown: false
        },
        {
          name: 'News',
          dropdown: true
        },
        {
          name: 'Pages',
          dropdown: true
        },
        {
          name: 'Contact',
          dropdown: false
        },
        {
          name: 'Purchase',
          dropdown: false
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
  background-color: $main-red;
  color: white;
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
    li{
      margin: 1rem;
    }
  }
  .menu-text{
    display: flex;
  }
}

</style>
