<template lang="html">
    <div>
        <heador/>
        <footor/>
        <navbar/>
    </div>
</template>

<script>
import Heador from "../public/header";
import Footor from "../public/footer";
import Navbar from "../public/navbar";
export default {
  components: {
    Heador,
    Footor,
    Navbar
  }
};
</script>

<style lang="scss" module>

</style>