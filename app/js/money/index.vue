<template lang="html">
    <div>
        <heador/>
        <slider/>
        <ticket/>
        <recommend/>
        <banner/> 
        <money/>     
        <footor :banner="banner"/>
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
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Ticket,
    Recommend,
    Banner,
    Money
  },
  data() {
    return {
      banner:
        "//img12.360buyimg.com/jrpmobile/jfs/t7162/219/4755741/18941/4e51a5aa/597b066dNf6c7a972.jpg?width=750&height=120"
    };
  }
};
</script>

<style lang="scss" module>

</style>