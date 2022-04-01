<template>
  <div id="app">
    <HeaderSec/>
    <MainSec2/>
    <SliderSec/>
  </div>
</template>

<script>
import HeaderSec from './components/ProjHeader.vue'
import MainSec2 from './components/ProjMain2.vue'
import SliderSec from './components/ProjMainSlider.vue'

export default {
  name: 'App',
  components: {
    HeaderSec,
    MainSec2,
    SliderSec
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss'
</style>
