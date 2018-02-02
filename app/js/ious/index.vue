<template lang="html">
    <div>
        <heador/>
        <slider/>
        <welfare/>
        <service/>
        <footor/>
        <navbar/>
    </div>
</template>

<script>
import Heador from "../public/header";
import Footor from "../public/footer";
import Navbar from "../public/navbar";
import Slider from './islider'
import Welfare from './welfare'
import Service from './service'
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Welfare,
    Service
  }
};
</script>

<style lang="scss" module>

</style>