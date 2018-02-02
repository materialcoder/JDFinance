<template lang="html">
    <div>
        <heador/>
        <slider/>
        <daily/>
        <in/>
        <more/>
        <footor cname="rfooter"/>
        <navbar/>
    </div>
</template>

<script>
import Heador from "../public/header";
import Footor from "../public/footer";
import Navbar from "../public/navbar";
import Slider from "./rslider"
import Daily from './daily'
import In from './in'
import More from './more'
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Daily,
    In,
    More
  }
};
</script>

<style lang="scss">
.rfooter {
  margin-top: 0 !important;
  ul {
    li:first-child {
      display: none;
    }
  }
}
</style>