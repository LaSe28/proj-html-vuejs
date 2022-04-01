<template>
<header>
  <div>
    <img src="../assets/img/theme_eduprime_logo.png" alt="">
  </div>
  <div>
    <ul>
      <li v-for="(ele, index) in navMenu" :key="index">{{ele.name}}</li>
    </ul>
    <button>VIEV COURSES</button>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderSec',
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

header{
  background-color: $main-red;
}

</style>
