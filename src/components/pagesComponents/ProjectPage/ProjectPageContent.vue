<template>
  <section class="project center">
    <ProjectPageCategories @activCategories="activCategories" />
    <ProjectPageProjects :projects="projectPage" />
    <div class="project__count-page">
      <div class="project__count-page-wrap">
        <router-link class="project__count-page-number" v-for="page in totalPages" :key="`p${page}`"
          :to="`/project/${page}`">
          <p class="project__count-page-number-text">{{ page }}</p>
        </router-link>
      </div>
    </div>
  </section>
</template>

<script>
import ProjectPageCategories from './ProjectPageCategories.vue'
import ProjectPageProjects from './ProjectPageProjects.vue'
export default {
  components: {
    ProjectPageCategories,
    ProjectPageProjects
  },
  name: 'ProjectPageContent',

  data () {
    return {
      quantity: 8,
      projects: [],
      projectsOne: [
        {
          id: 1,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 2,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 3,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 4,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 5,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 6,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 7,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 8,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 9,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 10,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 11,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 12,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 13,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 14,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 15,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 16,
          image: 'project__item_8.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        }
      ],
      projectsNew: [
        {
          id: 17,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 18,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 19,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 20,
          image: 'project__item_8.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 21,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 22,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 23,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 24,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 25,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 26,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 27,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 28,
          image: 'project__item_8.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 29,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 30,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 31,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 32,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        }
      ],
      projectsTwo: [
        {
          id: 33,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 34,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 35,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 36,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 37,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 38,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 39,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 40,
          image: 'project__item_8.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 41,
          image: 'project__item_5.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 42,
          image: 'project__item_2.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 43,
          image: 'project__item_3.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 44,
          image: 'project__item_4.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 45,
          image: 'project__item_1.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 46,
          image: 'project__item_6.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 47,
          image: 'project__item_8.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        },
        {
          id: 48,
          image: 'project__item_7.jpg',
          title: 'Minimal Bedroom',
          text: 'Decor / Artchitecture'
        }
      ]
    }
  },

  created () {
    this.projects = this.projectsOne
  },

  methods: {
    activCategories (data) {
      switch (data.id) {
        case 1:
          this.projects = this.projectsTwo
          break
        case 2:
          this.projects = this.projectsOne
          break
        case 3:
          this.projects = this.projectsNew
          break
        case 4:
          this.projects = this.projectsNew
          break
      }
    }
  },
  computed: {
    totalPages () {
      return Math.ceil(this.projects.length / this.quantity)
    },
    currentPage () {
      return this.$route.params.page || 1
    },
    projectPage () {
      const pageNumber = this.currentPage
      const startIndex = (pageNumber - 1) * this.quantity
      const endIndex = startIndex + this.quantity
      return this.projects.slice(startIndex, endIndex)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../../scss/vars";

.project {
  &__count-page {
    margin-top: 51px;
    margin-bottom: 200px;
    display: flex;
    justify-content: center;

    &-wrap {
      display: flex;
      gap: 20px;
    }

    &-number {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: nowrap;
      border: 1px #cda274 solid;
      width: 52px;
      height: 52px;
      border-radius: 52px;

      &-text {
        color: $primaryColor;
        font-family: $familyText;
        font-size: 16px;
        font-style: normal;
        font-weight: $font-500;
        line-height: 150%;
        text-transform: capitalize;
      }

      &:hover {
        background: #f4f0ec;
        border: none;
        width: 54px;
        height: 54px;
      }
    }

    &-svg:hover {
      fill: #f4f0ec;

      & circle {
        stroke: none;
      }
    }
  }
}
</style>
