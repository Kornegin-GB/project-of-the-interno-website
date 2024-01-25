<template>
  <Slide class="burger-menu" :right=true>
    <link-menu-component class="burger-menu" textColor="#fff" />
  </Slide>
</template>

<script>
import { Slide } from 'vue-burger-menu'
import LinkMenuComponent from './LinkMenuComponent.vue'

export default {
  name: 'BurgerMenuComponent',
  components: { Slide, LinkMenuComponent },

  mounted () {
    document.querySelector('.bm-burger-button').style.top = '65px'
  }
}
</script>

<style lang="scss" scoped>
.burger-menu {
  flex-direction: column;
  gap: 30px;
}
</style>
