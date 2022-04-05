<template>
<div class="main-container">
  <div class="container pb-5 pt-5">
    <div style="width: 30%">
      <img class="mb-2" src="../assets/img/theme_eduprime_logo.png" alt="">
      <p class="mb-1">EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
      <div class="icons">
        <div>
          <i class="fa-brands fa-facebook-f"></i>
        </div>
        <div>
          <i class="fa-brands fa-twitter"></i>
        </div>
        <div>
          <i class="fa-brands fa-instagram"></i>
        </div>
      </div>
    </div>
    <div style="width: 20%">
      <h4 class="mb-1">Get EduPrime</h4>
      <ul>
        <li v-for="(ele, index) in arrMenu1" :key="index">{{ele}}</li>
      </ul>
    </div>
    <div style="width: 20%">
      <h4 class="mb-1">Networking</h4>
      <ul>
        <li v-for="(ele, index) in arrMenu2" :key="index">{{ele}}</li>
      </ul>
    </div>
    <div style="width: 30%">
      <div class="input-container">
        <input placeholder="Search" type="text">
        <button class="btn btn-y"><i class="fa-solid fa-search"></i></button>
      </div>
      <div class="categories">
        <h5 class="mb-1 mt-2">Search categories</h5>
        <ul>
          <li v-for="(ele, index) in arrMenu3" :key="index">{{ele.toUpperCase()}}</li>
        </ul>
        <p class="mt-2">ModelTheme. All rights reserved. </p>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'FooterSec',
  data () {
    return {
      arrMenu1: [
        'Request a website',
        'Browse Themes',
        'Payment options',
        'Support System',
        'Checkout',
        'Purchase Theme'
      ],
      arrMenu2: [
        'Purchase Theme',
        'Our Benefits',
        'Our team',
        'Our Services',
        'Other Products',
        'My account'
      ],
      arrMenu3: [
        'economy',
        'design',
        'coaching',
        'business',
        'medicine',
        'law',
        'fitness'
      ]
    }
  }

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

.main-container{
  background-color: $main-red;
  color: white;
  .container{
    display: flex;
    img{
      height: 50px;
    }
    ul{
      list-style: none;
      li{
        margin: .5rem 0;
        &:hover{
          cursor: pointer;
        }
      }
    }
    .icons{
      display: flex;
      div{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40px;
        height: 40px;
        border: 1px solid $main-gold;
        padding: .5rem;
        border-radius: 50%;
        margin: .2rem;
        &:hover{
          background-color: white;
          color: $main-red;
          cursor: pointer;
        }
      }
    }
    .categories{
      text-align: right;
      ul{
        display: flex;
        justify-content: end;
        flex-wrap: wrap;
        li{
          font-size: .6rem;
          border: 1px solid white;
          padding: 0.4em 1em;
          border-radius: 1.5em;
          margin: .4em;
          &:hover{
            background-color: $main-gold;
            cursor: pointer;
          }
        }
      }
      p{
        color: $main-gold;
      }
    }
  }
}
.input-container{
      height: 2.5rem;
      background-color: white;
      border-radius: 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      &:focus-within{
        outline: 3px solid $main-gold;
      }
      .btn{
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        height: 2.7rem;
        width: 2.7rem;
      }
      input{
        border: none;
        outline: none;
        margin-left: 1rem;
      }
    }

</style>
