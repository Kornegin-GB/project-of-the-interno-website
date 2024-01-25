<template>
  <footer class="footer center">
    <div class="footer__logo">
      <logo-component />
      <p class="footer__logo-text">It is a long established fact that a reader will be distracted lookings.</p>
      <div class="footer__logo-icon">
        <router-link class="icon__link" to="vk">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd"
              d="M23.4493 5.94799C23.6161 5.40154 23.4493 5 22.6553 5H20.0297C19.3621 5 19.0543 5.34687 18.8874 5.72936C18.8874 5.72936 17.5521 8.92607 15.6606 11.0025C15.0487 11.6036 14.7705 11.7949 14.4367 11.7949C14.2698 11.7949 14.0194 11.6036 14.0194 11.0572V5.94799C14.0194 5.29225 13.8345 5 13.2781 5H9.15213C8.73494 5 8.48403 5.30434 8.48403 5.59278C8.48403 6.21441 9.42974 6.35777 9.52722 8.10641V11.9042C9.52722 12.7368 9.37413 12.8878 9.04032 12.8878C8.15023 12.8878 5.98507 9.67682 4.70093 6.00261C4.44927 5.28847 4.19686 5 3.52583 5H0.900218C0.150044 5 0 5.34687 0 5.72936C0 6.41244 0.890141 9.80039 4.14464 14.2812C6.31429 17.3412 9.37118 19 12.1528 19C13.8218 19 14.0283 18.6316 14.0283 17.997V15.6842C14.0283 14.9474 14.1864 14.8003 14.7149 14.8003C15.1043 14.8003 15.7719 14.9916 17.3296 16.467C19.1099 18.2156 19.4034 19 20.4047 19H23.0304C23.7805 19 24.1556 18.6316 23.9392 17.9045C23.7024 17.1799 22.8525 16.1286 21.7247 14.8823C21.1127 14.1719 20.1947 13.4069 19.9165 13.0243C19.5271 12.5326 19.6384 12.314 19.9165 11.8769C19.9165 11.8769 23.1155 7.45067 23.4493 5.94799Z"
              fill="black" />
          </svg>
        </router-link>
        <router-link class="icon__link" to="ok">
          <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none">
            <path
              d="M19.339 23.255c1.703-0.391 3.323-1.061 4.801-1.989 1.111-0.744 1.412-2.244 0.667-3.359-0.713-1.068-2.14-1.391-3.244-0.735-3.401 2.125-7.724 2.125-11.125 0-1.125-0.713-2.62-0.375-3.333 0.749 0 0.005 0 0.005 0 0.005-0.713 1.131-0.375 2.625 0.756 3.333l0.004 0.005c1.475 0.928 3.095 1.599 4.792 1.985l-4.62 4.619c-0.943 0.928-0.957 2.437-0.036 3.381l0.041 0.041c0.459 0.473 1.079 0.708 1.699 0.708s1.239-0.235 1.697-0.708l4.563-4.537 4.536 4.543c0.964 0.921 2.495 0.9 3.423-0.063 0.905-0.937 0.905-2.423 0-3.36zM16 16.516c4.563-0.005 8.255-3.699 8.26-8.256 0-4.552-3.708-8.26-8.26-8.26s-8.26 3.708-8.26 8.26c0.005 4.563 3.703 8.256 8.26 8.261zM16 4.844c1.885 0 3.416 1.531 3.416 3.416 0 1.891-1.531 3.417-3.416 3.423-1.885-0.005-3.416-1.532-3.421-3.423 0.005-1.885 1.536-3.416 3.421-3.421z"
              fill="black" />
          </svg>
        </router-link>
      </div>
    </div>
    <div class="footer__menu">
      <p class="footer__menu-title">Pages</p>
      <link-menu-component class="footer__link" textColor="#4D5053" />
    </div>
    <div class="footer__services"></div>
    <div class="footer__contact">
      <p class="footer__contact-title">Contact</p>
      <p class="footer__contact-text">55 East Birchwood Ave. Brooklyn, New York 11201</p>
      <p class="footer__contact-text-email">contact@interno.com</p>
      <p class="footer__contact-text">(123) 456 - 7890</p>
    </div>
  </footer>
</template>

<script>
import LogoComponent from '../components/LogoComponent.vue'
import LinkMenuComponent from './LinkMenuComponent.vue'
export default {
  components: { LogoComponent, LinkMenuComponent },
  name: 'FooterComponent',

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
@import "../scss/vars";

.icon__link:hover {
  path {
    opacity: 0.5;
    transition: $transitionLinc;
  }

}

.footer {
  // margin-top: 96px;
  padding-bottom: 134px;
  display: flex;
  gap: 101px;

  &__link {
    font-size: 22px;
    letter-spacing: 0.22px;
    line-height: 300%;
  }

  &__logo {
    width: 393px;

    &-text {
      margin-top: 18px;
      margin-bottom: 31px;
      color: $secondColor;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }

    &-icon {
      display: flex;
      align-items: center;
      gap: 54px;
    }
  }

  &__menu {
    width: 125px;

    & div {
      display: flex;
      flex-direction: column;
    }

    &-title {
      margin-bottom: 9px;
      color: $primaryColor;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
    }
  }

  &__services {
    width: 120px;
  }

  &__contact {
    width: 258px;

    &-title {
      margin-bottom: 26px;
      color: $primaryColor;
      font-family: $familyTitle;
      font-size: 25px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
    }

    &-text {
      color: $secondColor;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;

      &-email {
        color: $secondColor;
        font-family: $familyText;
        font-size: 22px;
        font-style: normal;
        font-weight: $font-400;
        letter-spacing: 0.22px;
        line-height: 300%;
      }
    }
  }
}
</style>
