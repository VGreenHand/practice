<template>
<Swiper
    :slides-per-view="1"
    :space-between="50"
    :modules="modules"
    :pagination="{ clickable: true }"
    :autoplay="{ delay: 1000, disableOnInteraction: false, pauseOnMouseEnter:true }"
  >
    <SwiperSlide><img src="../assets/logo.png" alt=""></SwiperSlide>
    <SwiperSlide><img src="../assets/logo.png" alt=""></SwiperSlide>
    <SwiperSlide><img src="../assets/logo.png" alt=""></SwiperSlide>
    <SwiperSlide><img src="../assets/logo.png" alt=""></SwiperSlide>
  </Swiper>
</template>

<script>
import { Pagination,Autoplay } from 'swiper';
import {Swiper,SwiperSlide} from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';

export default {
  name: 'HelloWorld',
  data(){
    return {
        modules: [Pagination,Autoplay]
    }
  },
  components: {
    Swiper,
    SwiperSlide
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
