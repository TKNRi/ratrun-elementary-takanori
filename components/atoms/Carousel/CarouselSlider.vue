<template>
  <div class="slider-inner">
    <Carousel @slide-start="slideFunction" ref="myCarousel">
      <Slide v-for="(image, key) in images" :key="key">
        <img :src="getImg(image)" alt="" />
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>
    <div class="gallery">
      <button
        @click="clickImg(key)"
        v-for="(image, key) in images"
        :key="key"
        :class="key == currentPage ? 'focused-img' : 'non-focused-img'"
      >
        <img :src="getImg(image)" alt="" />
      </button>
    </div>
  </div>
</template>

<script setup>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
const myCarousel = ref(null);
const currentPage = ref(0);
const props = defineProps({
  images: {
    type: Array,
    default: null,
  },
});
const slideFunction = ({ slidingToIndex }) => {
  currentPage.value = slidingToIndex;
};
const getImg = (file) => {
  return new URL(`../../../assets/img/${file}`, import.meta.url).href;
};
const clickImg = (carouselNum) => {
  // カルーセル番号変える
  myCarousel.value.slideTo(carouselNum);
};
</script>

<style lang="scss" scoped>
img {
  height: 300px;
  width: 500px;
  @include mobile {
    width: 100%;
    height: auto;
  }
}
.gallery {
  display: flex;
  gap: 20px;
  margin: 40px 0;
  justify-content: center;
  @include mobile {
    gap: 10px;
  }
  img {
    height: 80px;
    width: 120px;
    @include mobile {
      width: 60px;
      height: 40px;
    }
  }
  button: {
    background: #fff;
  }
  .focused-img {
    border: 1px solid red;
    background: #fff;
  }
  .non-focused-img {
    border: none;
    background: #fff;
  }
}
</style>