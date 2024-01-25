<template>
  <router-link class="header__logo" to="/">
    <img src="../assets/images/Logo.jpg" alt="logo">
    <p class="logo__text">Interno</p>
  </router-link>
</template>

<script>
export default {
  name: 'LogoComponent',

  data () {
    return {

    }
  },

  mounted () {

  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import "../scss/vars";

.header__logo {
  display: flex;
  flex-wrap: nowrap;
  flex-direction: row;
  align-items: center;
  gap: 10px;

  & img {
    width: 34px;
    height: 34px;
  }

  & p {
    font-size: 40px;
    font-family: $familyTitle;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    color: $primaryColor;
  }
}
</style>
