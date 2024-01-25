<template>
  <SliderCarousel class="slider" :image-list="sliderImage" />
</template>

<script>
import SliderCarousel from '../../sliderComponents/SliderCarousel.vue'

export default {
  name: 'ProjectDetailsSlider',
  components: {
    SliderCarousel
  },

  data () {
    return {
      sliderImage: [
        { id: 1, imageSrc: 'project_details_photo.jpg', imageAlt: 'image_1' },
        { id: 2, imageSrc: 'blog_image_4.jpg', imageAlt: 'image_2' },
        { id: 3, imageSrc: 'blog_image_5.jpg', imageAlt: 'image_3' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.hooper {
  height: 799px;
}

.slider {
  border-radius: 70px;
  overflow: hidden;
}
</style>
