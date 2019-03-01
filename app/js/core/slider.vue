<template lang="html">
    <section :class="cname">
        <swiper :options="options" >
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link to="{name:item.href}">
                    <img :src="item.src" alt=""></img>
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"></div>
        </swiper>
        
    </section>
</template>
<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  components: {
    swiper,
    swiperSlide
  },
  props: {
    cname: {
      type: String,
      default: ""
    },
    options: {
      type: Object,
      default: function() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination"
          }
        };
      }
    },
    items: {
      type: Array,
      default: function() {
        return [];
      }
    }
  }
};
</script>

<style lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>

