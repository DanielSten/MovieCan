<template>
  <div class="carousel">
    <swiper
        :cssMode="true"
        :keyboard="true"
        :spaceBetween="0"
        :centeredSlides="true"
        :autoplay="{
          delay: 50000,
          disableOnInteraction: false,
        }"
        :pagination="{
          clickable: true,
        }"
        :navigation="true"
        :modules="modules"
        class="mySwiper"
    >
      <swiper-slide><img style="height: 60vh;" src="./icons/poster1.jpg"></swiper-slide>
      <swiper-slide><img style="height: 60vh;" src="./icons/poster2.jpg"></swiper-slide>
      <swiper-slide><img style="height: 60vh;" src="./icons/poster3.jfif"></swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

import { Autoplay, Navigation, Pagination, Keyboard } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Navigation, Pagination, Keyboard],
    };
  },
};
</script>

<style scoped>
swiper {
  width: 100%;
  height: 100%;
  color: white;
}

swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}
.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 0 15%;
}
</style>
<style>
.carousel .mySwiper .swiper-pagination-bullet-active{
  background-color: #d2d2d2 !important;
}
.carousel .mySwiper .swiper-button-next:after{
  color: #d2d2d2 !important;
}
.carousel .mySwiper .swiper-button-prev:after{
  color: #d2d2d2 !important;
}
</style>