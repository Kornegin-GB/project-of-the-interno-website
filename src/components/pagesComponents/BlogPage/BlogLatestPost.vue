<template>
  <div class="latest-post__wrap">
    <img :src="require('@/assets/images/' + latestArticle.image)" width="569" height="478" alt="latest-post-img"
      class="latest-post__img">
    <div class="latest-post__content">
      <h3 class="latest-post__content-title">{{ latestArticle.itemTitle }}</h3>
      <p class="latest-post__content-text">Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis dignissim
        maximus.posuere in.Contrary to popular belief.</p>
      <p class="latest-post__content-text">Lorem Ipsum is not simply random text. It has roots in a piece of classica.</p>
      <div class="latest-post__content-wrap">
        <p class="latest-post__content-data">{{ latestArticle.itemData }}</p>
        <router-link class="button__link" to="/blog-details">
          <svg xmlns="http://www.w3.org/2000/svg" width="53" height="53" viewBox="0 0 53 53" fill="none">
            <circle cx="26.5" cy="26.267" r="26" fill="#F4F0EC" />
            <path d="M24.271 32.9525L30.2139 26.2668L24.271 19.5811" stroke="#292F36" stroke-width="2"
              stroke-linecap="round" stroke-linejoin="round" />
          </svg>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
const { articles } = require('@/assets/scripts/data.js')
export default {
  name: 'BlogLatestPost',

  data () {
    return {
      articles: articles
    }
  },

  mounted () {

  },

  methods: {

  },

  computed: {
    latestArticle () {
      return this.articles[this.articles.length - 1]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.button__link {
  & circle:hover {
    fill: #e1d6cc;
    transition: $transitionLinc;
  }
}

.latest-post {
  &__wrap {
    border: 1px solid #e7e7e7;
    display: flex;
    gap: 62px;
    padding: 22px;
    border-radius: 62px;
    align-items: center;
  }

  &__img {
    border-radius: 50px;
  }

  &__content {
    width: 489px;

    &-title {
      margin-bottom: 22px;
      color: $primaryColor;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
      letter-spacing: 0.5px;
    }

    &-text {
      margin-bottom: 41px;
      color: $secondColor;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }

    &-wrap {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: nowrap;
    }

    &-data {
      color: $secondColor;
      font-family: $familyText;
      font-size: 16px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.16px;
      text-transform: capitalize;
    }
  }
}
</style>
