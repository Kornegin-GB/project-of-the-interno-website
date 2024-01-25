<template>
  <div>
    <router-link class="menu__link" :style="{ color: textColor }" to="/">Home</router-link>
    <router-link class="menu__link" :style="{ color: textColor }" to="/project">Project</router-link>
    <router-link class="menu__link" :style="{ color: textColor }" to="/blog">Blog</router-link>
  </div>
</template>

<script>
export default {
  name: 'LinkMenuComponent',
  props: ['textColor']
}
</script>

<style lang="scss" scoped>
@import "../scss/vars";

.menu__link {
  font-family: $familyText;
  font-style: normal;
  font-weight: $font-400;

  &:hover {
    text-decoration-line: underline;
  }
}
</style>
