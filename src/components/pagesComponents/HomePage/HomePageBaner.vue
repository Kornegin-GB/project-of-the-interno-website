<template>
  <section class="baner center">
    <div class="baner__wrap">
      <div class="baner__wrap-content">
        <h1 class="baner__title">Let Your Home Be Unique</h1>
        <p class="baner__text">There are many variations of the passages of
          lorem Ipsum fromavailable, majority.</p>
        <a href="#" class="baner__button">
          <div class="baner__button-text">
            <p>Get Started</p>
            <img src="@/assets/images/row_left.svg" alt="row_left">
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomePageBaner'
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.baner {
  &__wrap {
    height: 758px;
    background-image: url("@/assets/images/Header_Photo.jpg");
    background-repeat: no-repeat;
    border-radius: 75px;
  }

  &__wrap-content {
    padding: 208px 700px 0 52px;
  }

  &__title {
    margin-bottom: 18px;
    color: $primaryColor;
    font-family: $familyTitle;
    font-size: 65px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
  }

  &__text {
    color: $secondColor;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
    margin-bottom: 21px;
  }

  &__button-text {
    width: 220px;
    padding: 26px 0;
    background-color: $primaryColor;
    border-radius: 18px;
    display: flex;
    gap: 10px;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;

    & p {
      color: #fff;
      font-family: $familyText;
      font-size: 18px;
      font-style: normal;
      font-weight: 600;
      line-height: 125%;
      letter-spacing: 0.36px;
    }
  }
}

@media (max-width: 1199px) {
  .baner {
    &__wrap-content {
      padding: 208px 500px 0 52px;
    }
  }
}

@media (max-width: 1023px) {

  .baner {
    &__wrap-content {
      padding: 208px 270px 0 52px;
    }
  }
}

@media (max-width: 767px) {
  .baner {
    &__wrap {
      height: 360px;
    }

    &__wrap-content {
      padding: 40px 50px;
    }

    &__title {
      font-size: 32px;
    }

    &__text {
      font-size: 18px;
    }
  }
}

@media (max-width: 359px) {
  .baner {
    &__wrap {
      height: 340px;
    }

    &__wrap-content {
      padding: 40px 35px;
    }

    &__button-text {
      width: 200px;
      padding: 16px 0;

      & p {
        font-size: 16px;
      }
    }
  }
}
</style>
