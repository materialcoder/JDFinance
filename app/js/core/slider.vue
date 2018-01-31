<template lang="html">
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slider v-for="item in items" :key="item.href">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slider>
            <div class="swiper-pagination" v-if="options.pagination"></div>
        </swiper>
    </section>
</template>

<script>
import { swiper, swiperSlider } from "vue-awesome-swiper";
export default {
  components: {
    swiper,
    swiperSlider
  },
  props: {
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination"
          },
          notNextTick: false
        };
      }
    },
    items: {
      type: Array,
      default() {
        return [];
      }
    }
  }
};
</script>

<style lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>