<template>
  <hooper :settings="settingsSlider">

    <slide v-for="image in imageList" :key="image.id">
      <img @click="onClickImg($event.target)" class="carousel__item-img"
        :src="require('@/assets/images/' + image.imageSrc)" :alt="image.imageAlt">
    </slide>
    <Pagination slot="hooper-addons" mode></Pagination>
  </hooper>
</template>

<script>
import { Hooper, Slide, Pagination } from 'hooper'
import 'hooper/dist/hooper.css'

export default {
  name: 'SliderCarousel',
  props: ['imageList'],
  components: {
    Hooper,
    Slide,
    Pagination
  },
  data () {
    return {
      settingsSlider: {
        itemsToShow: 1,
        infiniteScroll: true
      }
    }
  },

  mounted () {
    const indicator = document.querySelectorAll('.hooper-pagination')
    indicator.forEach((element) => {
      element.setAttribute('style', 'font-size: 40px; font-weight: bold; background: silver; opacity: 0.6')
    })
  },

  methods: {
    onClickImg (image) {
      window.open(image.src)
    }
  }
}

</script>

<style lang="scss" scoped>
.carousel__item-img {
  width: 100%;
  position: absolute;
  bottom: -300px;
}
</style>
