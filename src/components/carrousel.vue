<template>
  <swiper
    :slides-per-view="3"
    :space-between="50"
    navigation
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide>
      <h2>Slide 1</h2>
      <p>--------</p>
      <p>--------</p>
      <p>--------</p>
      <p>--------</p>
    </swiper-slide>
    <swiper-slide>
      <h2>Slide 2</h2>
    </swiper-slide>
    <swiper-slide>
      <h2>Slide 3</h2>
    </swiper-slide>
    <swiper-slide>
      <h2>Slide 4</h2>
    </swiper-slide>
    <swiper-slide>
      <h2>Slide 5</h2>
    </swiper-slide>
    <swiper-slide>
      <h2>Slide 6</h2>
    </swiper-slide>
  </swiper>
</template>
<script>

import SwiperCore, { Navigation, Pagination, A11y } from 'swiper'

import { Swiper, SwiperSlide } from 'swiper/vue'

import 'swiper/swiper.scss'
import 'swiper/components/navigation/navigation.scss'
import 'swiper/components/pagination/pagination.scss'

SwiperCore.use([Navigation, Pagination, A11y])

export default {
  components: {
    Swiper,
    SwiperSlide
  },
  methods: {
    onSwiper (swiper) {
      // console.log(swiper)
    },
    onSlideChange () {
      // console.log('slide change')
    }
  }
}
</script>
