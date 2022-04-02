<template>
  <div id="app">
    <HeaderSec/>
    <MainSec2/>
    <SliderSec/>
    <MainSec3/>
  </div>
</template>

<script>
import HeaderSec from './components/ProjHeader.vue'
import MainSec2 from './components/ProjMain2.vue'
import SliderSec from './components/ProjMainSlider.vue'
import MainSec3 from './components/ProjMain3.vue'

export default {
  name: 'App',
  components: {
    HeaderSec,
    MainSec2,
    SliderSec,
    MainSec3
  }
}
</script>

<style lang="scss">
@import './assets/styles/style.scss'
</style>
