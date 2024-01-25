<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import "scss/vars";

* {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

.center {
  padding-left: calc(50% - $widthSite / 2);
  padding-right: calc(50% - $widthSite / 2);
}

@media (max-width: 1199px) {
  $widthSite: 1024px;

  .center {
    padding-left: calc(50% - $widthSite / 2);
    padding-right: calc(50% - $widthSite / 2);
  }
}

@media (max-width: 1023px) {
  $widthSite: 768px;

  .center {
    padding-left: calc(50% - $widthSite / 2);
    padding-right: calc(50% - $widthSite / 2);
  }
}

@media (max-width: 767px) {
  $widthSite: 425px;

  .center {
    padding-left: calc(50% - $widthSite / 2);
    padding-right: calc(50% - $widthSite / 2);
  }
}

@media (max-width: 424px) {
  $widthSite: 360px;

  .center {
    padding-left: calc(50% - $widthSite / 2);
    padding-right: calc(50% - $widthSite / 2);
  }
}

@media (max-width: 359px) {
  $widthSite: 320px;

  .center {
    padding-left: calc(50% - $widthSite / 2);
    padding-right: calc(50% - $widthSite / 2);
  }
}
</style>
