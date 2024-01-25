<template>
  <section class="latest-post center">
    <h2 class="latest-post__title">Latest Post</h2>
    <BlogLatestPost />
  </section>
</template>

<script>
import BlogLatestPost from './BlogLatestPost.vue'
export default {
  components: { BlogLatestPost },
  name: 'BlogPageLastPost',

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
@import "@/scss/vars";

.latest-post {
  &__title {
    margin-top: 200px;
    margin-bottom: 27px;
    color: $primaryColor;
    font-family: $familyTitle;
    font-size: 50px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 1px;
  }
}
</style>
