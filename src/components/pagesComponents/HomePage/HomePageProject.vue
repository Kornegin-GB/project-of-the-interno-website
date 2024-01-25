<template>
  <section class="project center">
    <h2 class="project__title">Follow Our Projects</h2>
    <p class="project__text">It is a long established fact that a reader will be distracted by the of readable content
      of page lookings at its layouts points.</p>
    <div class="project__item-wrap">
      <div class="project__item" v-for="project in projectList" :key="project.id">
        <img :src="require('@/assets/images/' + project.img)" :alt="project.img"
          :class="'project__item-img ' + project.class">
        <div class="project__item-content">
          <router-link to="/project" class="item__text-wrap">
            <h2 class="project__item-title">{{ project.title }}</h2>
            <p class="project__item-text">{{ project.text }}</p>
          </router-link>
          <router-link to="/project">
            <svg class="button__link" xmlns="http://www.w3.org/2000/svg" width="70" height="70" viewBox="0 0 53 53"
              fill="none">
              <circle cx="26.5" cy="26.267" r="26" fill="#F4F0EC" />
              <path d="M24.271 32.9525L30.2139 26.2668L24.271 19.5811" stroke="#292F36" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round" />
            </svg>
          </router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomePageProject',

  data () {
    return {
      projectList: [
        {
          id: 0,
          img: 'image_1.jpg',
          class: 'project__item-img-1',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture'
        },
        {
          id: 1,
          img: 'image_2.jpg',
          class: 'project__item-img-2',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture'
        },
        {
          id: 2,
          img: 'image_3.jpg',
          class: 'project__item-img-3',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture'
        },
        {
          id: 3,
          img: 'image_4.jpg',
          class: 'project__item-img-4',
          title: 'Modern Kitchan',
          text: 'Decor / Artchitecture'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.button__link circle:hover {
  fill: #e1d6cc;
  transition: $transitionLinc;
}

.project {
  margin-top: 96px;
  margin-bottom: 96px;

  &__title {
    margin-bottom: 8px;
    color: $primaryColor;
    text-align: center;
    font-family: $familyTitle;
    font-size: 50px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 1px;
  }

  &__text {
    padding-left: calc(($widthSite - 760px) / 2);
    padding-right: calc(($widthSite - 760px) / 2);
    color: $secondColor;
    text-align: center;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }

  &__item-wrap {
    margin-top: 93px;
    display: grid;
    column-gap: 100px;
    row-gap: 56px;
    grid-template-columns: repeat(2, ($widthSite - 100) / 2);
  }

  &__item-img {
    width: 100%;
  }

  &__item-img-1 {
    border-top-right-radius: 75px;
  }

  &__item-img-2 {
    border-top-left-radius: 75px;
  }

  &__item-img-3 {
    border-bottom-right-radius: 75px;
  }

  &__item-img-4 {
    border-bottom-left-radius: 75px;
  }

  &__item-content {
    margin-top: 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__item-title {
    color: $primaryColor;
    font-family: $familyTitle;
    font-size: 25px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 0.5px;
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

.item__text-wrap:hover {
  opacity: $opacityLink;
  transition: $transitionLinc;
}

@media (max-width: 1199px) {
  $widthSite: 1024px;

  .project {
    &__text {
      padding-left: calc(($widthSite - 760px) / 2);
      padding-right: calc(($widthSite - 760px) / 2);
    }

    &__item-wrap {
      grid-template-columns: repeat(2, ($widthSite - 100) / 2);
    }
  }
}

@media (max-width: 1023px) {
  $widthSite: 768px;

  .project {

    &__text {
      padding-left: calc(($widthSite - 760px) / 2);
      padding-right: calc(($widthSite - 760px) / 2);
    }

    &__item-wrap {
      gap: 50px;
      grid-template-columns: repeat(2, ($widthSite - 50) / 2);
    }
  }
}

@media (max-width: 767px) {
  $widthSite: 425px;

  .project {
    margin-top: 56px;

    &__title {
      font-size: 30px;
    }

    &__text {
      padding-left: 5px;
      padding-right: 5px;
      font-size: 18px;
    }

    &__item-wrap {
      margin-top: 63px;
      row-gap: 50px;
      column-gap: 0;
      grid-template-columns: repeat(1, $widthSite);
    }
  }
}

@media (max-width: 424px) {
  $widthSite: 360px;

  .project {
    &__item-wrap {
      grid-template-columns: repeat(1, $widthSite);
    }
  }
}

@media (max-width: 359px) {
  $widthSite: 320px;

  .project {
    &__item-wrap {
      grid-template-columns: repeat(1, $widthSite);
    }
  }
}
</style>
