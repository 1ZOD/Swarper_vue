<template>
  <swiper
    :slides-per-view="4.16"
    :space-between="10"
    :free-mode="true"
    :loop="true"
    class="my-swiper"
  >
    <swiper-slide v-for="(movie, index) in movies" :key="index">
      <img :src="movie.image" alt="Movie Poster" class="movie-image" />
    </swiper-slide>
  </swiper>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';

const movies = ref<{ image: string }[]>([
  { image: 'https://imgur.com/ym8Tjdu.png' },
  { image: 'https://imgur.com/tY3sbBZ.png' },
  { image: 'https://imgur.com/KEfW1tG.png' },
  { image: 'https://imgur.com/FCjuQ8I.png' },
  { image: 'https://imgur.com/aGU3SSJ.png' },
  { image: 'https://imgur.com/FdQR9.png'   },
  { image: 'https://imgur.com/zagqBk6.png' },
  { image: 'https://imgur.com/PdZb6FX.png' },
  { image: 'https://imgur.com/uAHASJ0.png' },
]);

</script>

<style scoped>
.my-swiper {
  width: 100%;
  height: 100%;
}

.movie-image {
  width: 100%;
  height: 30rem;
  border-radius: 10px;
}
</style>
