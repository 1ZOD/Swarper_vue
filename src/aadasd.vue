<template>
  <swiper
    :slides-per-view="4"
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
  { image: 'https://i.imgur.com/GL7igry.png' },
  { image: 'https://i.imgur.com/GL7igry.png' },
  { image: 'https://i.imgur.com/GL7igry.png' },
  { image: 'https://i.imgur.com/GL7igry.png' },
  { image: 'https://i.imgur.com/GL7igry.png' },
  { image: 'https://i.imgur.com/GL7igry.png' },
]);

</script>

<style scoped>
.my-swiper {
  width: 100%;
  height: 100%;
}

.movie-image {
  width: 100%;
  border-radius: 10px;
}
</style>
