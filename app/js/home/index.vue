<template lang="html">
    <div>
        <heador/>
        <slider/>
        <novice/>
        <borrow/>
        <money/>
        <product/>
        <life/>
        <footor :banner="banner"/>
        <navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue";
import Footor from "../public/footer";
import Navbar from "../public/navbar";
import Slider from "./hslider";
import Novice from "./novice";
import Borrow from "./borrow";
import Money from "./money";
import Product from "./product";
import Life from "./life";
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Novice,
    Borrow,
    Money,
    Product,
    Life
  },
  data() {
    return {
      banner:
        "//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252"
    };
  }
};
</script>

<style lang="scss" module>

</style>
