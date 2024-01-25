<template>
  <header class="header center">
    <logo-component />
    <burger-menu-component />
    <link-menu-component class="header__menu" textColor="#292F36" />
  </header>
</template>

<script>
import BurgerMenuComponent from './BurgerMenuComponent.vue'
import LinkMenuComponent from './LinkMenuComponent.vue'
import LogoComponent from './LogoComponent.vue'

export default {
  components: { LogoComponent, LinkMenuComponent, BurgerMenuComponent },
  name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
@import "../scss/vars";

.burger-menu {
  display: none;
}

.header {
  margin-top: 53px;
  margin-bottom: 57px;
  font-family: $familyTitle;
  display: flex;
  flex-direction: row;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-between;

  &__menu {
    font-size: 20px;
    line-height: 125%;
    display: flex;
    gap: 48px;
  }
}

@media (max-width: 767px) {
  .header {
    &__menu {
      gap: 18px;
    }
  }
}

@media (max-width: 424px) {
  .header {
    &__menu {
      display: none;
    }
  }

  .burger-menu {
    display: block;
  }
}
</style>
