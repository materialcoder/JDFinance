<template lang="html">
    <div>
        <heador/>
        <slider/>
        <ticket/>
        <recommend/>
        <banner/> 
        <money/>
        <fbanner/>
        <footor cname="mfooter"/>
        <navbar/>
    </div>
</template>

<script>
import Heador from "../public/header";
import Footor from "../public/footer";
import Navbar from "../public/navbar";
import Slider from "./mslider";
import Ticket from "./ticket";
import Recommend from "./recommend";
import Banner from "./banner";
import Money from "./money";
import Fbanner from "./fbanner";
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Ticket,
    Recommend,
    Banner,
    Money,
    Fbanner
  }
};
</script>

<style lang="scss">
.mfooter {
  margin-top: 0 !important;
  ul {
    li:first-child {
      display: none;
    }
  }
}
</style>