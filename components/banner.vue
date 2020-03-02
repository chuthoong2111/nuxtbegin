<template>
  <div class="carousel-wrapper">
    <VueSlickCarousel v-bind="slickOptions">
      <div v-for="i in 5" :key="i" class="img-wrapper">
        <img :src="`./${i}-200x100.jpg`" />
      </div>
      <template #prevArrow="arrowOption">
        <div class="custom-arrow btn-prew">
          {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
        </div>
      </template>
      <template #nextArrow="arrowOption">
        <div class="custom-arrow btn-next">
          {{ arrowOption.currentSlide }}/{{ arrowOption.slideCount }}
        </div>
      </template>
      <template #customPaging="page">
        <div class="custom-dot">
          {{ page }}
        </div>
      </template>
    </VueSlickCarousel>
  </div>
</template>

<script>
import Vue from 'vue'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
// optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
Vue.component('VueSlickCarousel', VueSlickCarousel)
export default {
  data() {
    return {
      slickOptions: {
        dots: true,
        lazyLoad: 'ondemand',
        arrows: true,
        arrowsClass: 'slick-arrow slick-prev custom-prev-class',
        dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        fade: true,
        infinite: true,
        speed: 500,
        slidesToShow: 2,
        slidesToScroll: 1
      }
    }
  }
}
</script>

<style>
.carousel-wrapper {
  padding: 40px;
}
.img-wrapper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>
