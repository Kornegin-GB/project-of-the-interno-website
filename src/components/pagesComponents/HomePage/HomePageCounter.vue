<template>
  <section class="counter center">
    <div class="counter__wrap">
      <div class="counter__item">
        <h2 class="counter__item-title">12</h2>
        <p class="counter__item-text">Years Of Experiance</p>
      </div>
      <div class="counter__item">
        <h2 class="counter__item-title">85</h2>
        <p class="counter__item-text">Success Project</p>
      </div>
      <div class="counter__item">
        <h2 class="counter__item-title">15</h2>
        <p class="counter__item-text">Active Project</p>
      </div>
      <div class="counter__item">
        <h2 class="counter__item-title">95</h2>
        <p class="counter__item-text">Happy CUstomers</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomePageCounter'
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.counter {
  padding-top: 151px;
  padding-bottom: 151px;
  background-color: #f4f0ec;

  // &__wrap {
  //   padding-left: 59px;
  //   padding-right: 59px;
  // }

  &__wrap {
    // display: flex;
    // justify-content: space-between;
    // flex-wrap: wrap;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }

  &__item {
    text-align: center;
    display: flex;
    row-gap: 16px;
    flex-direction: column;

    & {
      display: inline-block;
      border-right: 1px solid #cda274;
      // padding-right: 60px;
    }

    &:last-child {
      border-right: none;
    }
  }

  &__item-title {
    color: #cda274;
    font-family: $familyTitle;
    font-size: 85px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 1.7px;
  }

  &__item-text {
    color: $secondColor;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }
}

@media (max-width: 1023px) {
  $widthSite: 768px;

  .counter {
    &__wrap {
      grid-template-columns: repeat(2, 1fr);
    }

    &__item {

      &:nth-child(3),
      &:last-child {
        padding-top: 100px;
      }

      &:nth-child(2) {
        border-right: none;
      }
    }
  }
}
</style>
