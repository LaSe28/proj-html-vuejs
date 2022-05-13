<template>
<div>
  <div class="fixed">
    <div class="fixed-text">
      <a @click.prevent="" href="#!"><img src="../assets/svg/svg-3.svg" alt="">Purchase Theme</a>
    </div>
    <div class="fixed-text">
      <a @click.prevent="" href="#!"><img class="" src="../assets/svg/svg-2.svg" alt="">Related Themes</a>
    </div>
  </div>
  <div  @click="scroll()" class="fixed-icon">
    <i class="fa-solid fa-chevron-up"></i>
  </div>
  <div class="help-fixed">
    <i id="icon1" @click="toggleClassCart" class="fa-solid fa-cart-shopping"></i>
    <i id="icon2" @click="toggleClassInfo" class="fa-solid fa-book-open"></i>
    <i id="icon3" @click="toggleClassHelp" class="fa-solid fa-life-ring"></i>
  </div>
  <img class="background" :src="arrSlider[i]" alt="">
  <header @click="toggleDropdown(null, $event)" class="p-relative">
    <div class="p-2 nav">
      <img src="../assets/img/theme_eduprime_logo.png" alt="">
      <div class="menu-text">
        <ul>
          <li class="dropdown-parent ml-1 mr-1 toggler" @click="toggleDropdown(index, $event)" v-for="(ele, index) in navMenu" :key="index">
            {{ele.name}} <span v-if="ele.dropdown === true"><i class="fa-solid fa-chevron-down"></i></span>
            <div v-if="ele.dropdown === true ? index === navIndex : ''" class="dropdown">
              <ul>
                <li>opzione1 --------------</li>
                <li>opzione2 --------------</li>
                <li>opzione3 --------------</li>
              </ul>
            </div>
          </li>
        </ul>
      </div>
      <button class="btn btn-y">VIEW COURSES</button>
    </div>
    <MainSec1/>
    <img style="position: absolute; bottom: 0; width: 100%;" src="../assets/img/Wave-1.png" alt="">
  </header>
</div>
</template>

<script>
import MainSec1 from './ProjMain1.vue'
import img1 from '../assets/img/theme_slider1_bg-1.jpg'
import img2 from '../assets/img/theme_slider2_bg-1.jpg'
import img3 from '../assets/img/theme_slider3_bg-1.jpg'

export default {
  name: 'HeaderSec',
  components: {
    MainSec1
  },
  data () {
    return {
      navIndex: null,
      i: 0,
      arrSlider: [
        img1,
        img2,
        img3
      ],
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
  },
  methods: {
    incIndex () {
      if (this.i < this.arrSlider.length - 1) {
        this.i++
      } else {
        this.i = 0
      }
    },
    startSlider () {
      setInterval(this.incIndex, 4000)
    },
    toggleDropdown (index, event) {
      console.log(event)
      if (event.target.closest('.toggler')) {
        if (index !== null) {
          if (this.navIndex === index) {
            this.navIndex = null
          } else {
            this.navIndex = index
          }
        }
      } else {
        this.navIndex = index
      }
    },
    toggleClassCart () {
      document.querySelector('#icon1').classList.toggle('cart')
    },
    toggleClassInfo () {
      document.querySelector('#icon2').classList.toggle('info')
    },
    toggleClassHelp () {
      document.querySelector('#icon3').classList.toggle('help')
    },
    scroll () {
      window.scrollTo({ top: 0, behavior: 'smooth' })
    }
  },
  mounted () {
    this.startSlider()
  }

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

header{
  background-color: $main-red-tras;
  color: white;
  height:700px;
}
.cart::after{
  content: 'Carrello acquisti';
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 50px;
  padding: 2rem;
  position: absolute;
  left: 40px;
  border-radius: 1rem;
  background-color: $main-gold;
  color: $text-blue;
}
.info::after{
  content: 'info';
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 50px;
  padding: 2rem;
  position: absolute;
  left: 40px;
  border-radius: 1rem;
  background-color: $main-gold;
  color: $text-blue;
}
.help::after{
  content: 'Help';
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 50px;
  padding: 2rem;
  position: absolute;
  left: 40px;
  border-radius: 1rem;
  background-color: $main-gold;
  color: $text-blue;
}
.fixed{
  position: fixed;
  bottom: 1rem;
  left: 1rem;
  z-index: 11;
  .fixed-text{
    box-shadow: 0px 15px 10px -10px black;
    font-size: 0.8rem;
    display: flex;
    justify-content: center;
    height: 30px;
    width: 150px;
    padding: 0.4em .5em;
    margin: .5rem;
    background-color: #454545;
    border-radius: .3rem;
    img{
      height: 15px;
    }
    a{
      display: flex;
      align-items: center;
      color: white;
      text-decoration: none;
    }
  }
}
.fixed-icon{
  position: fixed;
  z-index: 11;
  bottom: 2rem;
  right: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 35px;
  width: 35px;
  background-color: $main-gold;
  border-radius: 50%;
  i{
    color: white;
  }
}
.help-fixed{
  position: fixed;
  z-index: 10;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: $main-gold;
  border-top-right-radius: .5rem;
  border-bottom-right-radius: .5rem;
  padding: .7rem;
  color: white;
  i{
    margin: 0.7rem 0;
    &:hover{
      cursor: pointer;
      color: $main-red;
    }
  }
}
.background{
  width: 100%;
  height: 700px;
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
    &:hover{
      cursor: pointer;
    }
  }
  .btn:hover{
    background-color: white;
    color: $main-red;

  }
}
.dropdown-parent{
  position: relative;
  &:hover{
    color: $main-gold;
  }
}
.dropdown{
  position: absolute;
  z-index: 10;
  left: -3rem;
  width: 250px;
  border-radius: .5rem;
  background-color: white;
  color: $main-red;
  ul{
    display: flex;
    flex-direction: column;
  }
  li{
    padding: 1rem;
    margin: .3rem;
    border-radius: .5rem;
  }
  li:hover{
    cursor: pointer;
    background-color: $main-red;
    color: white;
  }
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
