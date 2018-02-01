<template lang="html">
    <div>
        <heador/>
        <slider/>
        <novice/>
    </div>
</template>

<script>
import Heador from '../public/header.vue'
import Slider from './hslider'
import Novice from './novice'
export default {
  components: {
    Heador,
    Slider,
    Novice
  }
}
</script>

<style lang="scss" module>
  
</style>
