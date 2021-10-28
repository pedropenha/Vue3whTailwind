<template>
  <swiper
    :slides-per-view="3"
    :space-between="50"
    navigation
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
    v-for="images of img" v-bind:key="images"
  >
    <swiper-slide>
      <img :src="images"/>
    </swiper-slide>
  </swiper>
</template>
<script>

import SwiperCore, { Navigation, Pagination, A11y } from 'swiper'
import dados from './dados.json'

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
  data () {
    return {
      img: []
    }
  },
  methods: {
    onEnter () {
      console.log(dados)
    },
    onSwiper (swiper) {
      // console.log(swiper)
    },
    onSlideChange () {
      // console.log('slide change')
    }
  },
  mounted () {
    // for (let i = 0; i < dados.Insta.length; i++) {
    for (let i = 0; i < 3; i++) {
      console.log(dados.Insta[i].url)
      this.img.push(dados.Insta[i].url)
    }
  }
}
</script>
