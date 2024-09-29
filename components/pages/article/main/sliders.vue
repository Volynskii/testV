<script setup lang="ts">
  import { ref, onMounted } from 'vue';
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  import 'swiper/css/free-mode';
  import 'swiper/css/navigation';
  import 'swiper/css/thumbs';

  // import required modules
  import { FreeMode, Navigation, Thumbs } from 'swiper/modules';

  const thumbsSwiper = ref<Swiper | null>(null);

  // onMounted(() => {
  //   const swiper = {
  //     el: document.querySelector('.mySwiper'),
  //     // опции слайдера
  //   };
  //   thumbsSwiper.value = swiper;
  // });

  const setThumbsSwiper = (swiper: Swiper) => {
    thumbsSwiper.value = swiper;
  };
</script>

<template>
  <div class="article__sliders">
    <Swiper
      :style="{
        '--swiper-navigation-color': '#fff',
        '--swiper-pagination-color': '#fff',
      }"
      :loop="true"
      :navigation="false"
      :thumbs="{ swiper: thumbsSwiper }"
      :spaceBetween="10"
      :modules="[FreeMode, Navigation, Thumbs]"
      class="article__slider_first"
    >
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/1.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/2.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/3.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/4.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/5.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/7.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/8.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/9.jpg" /></SwiperSlide>
    </Swiper>

    <Swiper
      @swiper="setThumbsSwiper"
      :slidesPerView="4"
      :freeMode="true"
      :watchSlidesProgress="true"
      :spaceBetween="10"
      :modules="[FreeMode, Navigation, Thumbs]"
      class="article__slider_second"
    >
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/1.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/2.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/3.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/4.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/5.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/6.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/7.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/8.jpg" /></SwiperSlide>
      <SwiperSlide ><img src="https://cdn-st1.smotrim.ru/vh/pictures/xw/334/156/9.jpg" /></SwiperSlide>
    </Swiper>
  </div>
</template>


<style lang="scss">
  .article__sliders {
    width: 540px;

    img {
      width: 100%;
    }

    .article__slider_first {
      margin-bottom: 8px;
      .swiper-slide {
        border-radius: 16px;
        overflow: hidden;
      }
    }

    .article__slider_second {
      .swiper-slide {
        border-radius: 12px;
        overflow: hidden;
      }
    }
  }

  // .mySwiper {

  //   .swiper-wrapper {
  //   }

  //   .swiper-slide {
  //     overflow: hidden;
  //     border-radius: 16px;
  //   }
  // }

  // .wwww {
  //   width: 1000px;

  //   img {
  //     width: 100%;
  //   }
  // }
</style>