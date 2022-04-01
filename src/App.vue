<template>
  <div id="app">
    <HeaderSec/>
    <MainSec1/>
    <SliderSec/>
  </div>
</template>

<script>
import HeaderSec from './components/ProjHeader.vue'
import MainSec1 from './components/ProjMain1.vue'
import SliderSec from './components/ProjMainSlider.vue'

export default {
  name: 'App',
  components: {
    HeaderSec,
    MainSec1,
    SliderSec
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss'
</style>
