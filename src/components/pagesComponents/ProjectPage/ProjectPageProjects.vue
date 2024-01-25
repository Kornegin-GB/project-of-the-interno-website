<template>
  <div class="project__items">
    <div class="project__item" v-for="project in projects" :key="project.id">
      <img class="project__item-img" :src="require('@/assets/images/project_item/' + project.image)" alt="">
      <LikeComponent class="like" />
      <div class="project__item-wrap">
        <router-link to="/project-details" class="project__item-wrap-text">
          <h2 class="project__item-title">{{ project.title }}</h2>
          <p class="project__item-text">{{ project.text }}</p>
        </router-link>
        <router-link class="button__link" to="/project-details">
          <svg xmlns="http://www.w3.org/2000/svg" width="70" height="70" viewBox="0 0 70 70" fill="none">
            <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
            <path d="M32 44L40 35L32 26" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import LikeComponent from '../../LikeComponent.vue'
export default {
  components: { LikeComponent },
  name: 'ProjectPageProjects',
  props: ['projects'],

  data () {
    return {

    }
  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.like {
  position: absolute;
  top: 5px;
  right: 5px;
}

.button__link circle:hover {
  fill: #e1d6cc;
  transition: $transitionLinc;
}

.project__items {
  margin-top: 61px;
  margin-bottom: 61px;
  column-count: 2;
}

.project__item {
  position: relative;
  padding-bottom: 27px;
  display: inline-block;

  &-wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
    flex-direction: row;

    &-text:hover {
      opacity: $opacityLink;
      transition: $transitionLinc;
    }
  }

  &-title {
    color: $primaryColor;
    font-family: $familyTitle;
    font-size: 25px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 0.5px;
  }

  &-text {
    color: $secondColor;
    font-family: $familyText;
    font-size: 22px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.22px;
  }
}
</style>
