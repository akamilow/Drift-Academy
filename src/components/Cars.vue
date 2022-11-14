<template>
  <div class="cars-container">
      <div>
          <h2 class="title-section">Choose your car!</h2>
          <!-- <iframe id="video" width="750" height="420" src="https://www.youtube.com/embed/J252oda1N8s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
      </div>
      <swiper
          :slidesPerView="1"
          :spaceBetween="30"
          :loop="true"
          :autoplay="{
              delay: 10000,
              disableOnInteraction: false,
          }"
          :pagination="{
              clickable: true,
          }"
          :navigation="true"
          :modules="modules"
          class="mySwiper"
        >
        <swiper-slide>
          <img src="@/assets/img/rx7.jpg">
        </swiper-slide>
        <swiper-slide>
          <img src="@/assets/img/gtr-r34.jpg">
        </swiper-slide>
        <swiper-slide>
          <img src="@/assets/img/s15.jpg">
        </swiper-slide>
      </swiper>
  </div>
  <div>
    <h2 class="title-section">Choose your car!</h2>
    <h3 class="description-hero">Lorem ipsum dolor sit amet consectetur adipiscing elit, rhoncus fusce nam feugiat massa tellus euismod, lobortis tortor class in ut inceptos. Ridiculus viverra dapibus.</h3>
  </div>
  <div class="hero" id="hero">
    <div class="container">
        <hgroup>
            <h1 class="title-hero"><span class="first-title">Become a master</span>Drift Academy</h1>
            <h3 class="description-hero">Lorem ipsum dolor sit amet consectetur adipiscing elit, rhoncus fusce nam feugiat massa tellus euismod, lobortis tortor class in ut inceptos. Ridiculus viverra dapibus.</h3>
        </hgroup>
        <figure>
            <img class="image-hero img-responsive" src="@/assets/img/s15.jpg">
        </figure>
    </div>
  </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Autoplay, Pagination, Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>

<style>
.swiper {
  width: 800px;
  height: 400px;
  margin-left: auto;
  margin-right: auto;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.swiper-button-next, .swiper-button-prev {
    color: #e79c12;
    font-weight: bold;
}

.swiper-pagination-bullet-active {
    background-color: #e79c12;
}
</style>