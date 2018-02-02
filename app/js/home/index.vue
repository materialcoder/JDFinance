<template lang="html">
    <div>
        <heador/>
        <slider/>
        <novice/>
        <borrow/>
        <money/>
        <product/>
        <life/>
        <footor/>
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
  }
};
</script>

<style lang="scss" module>

</style>
