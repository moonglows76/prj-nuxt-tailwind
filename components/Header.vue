<template>
  <div class="header flex justify-between font-noto md:items-center">
    <h1 class="header__logo pt-5 pl-5 pb-[19px] md:pt-7 md:pl-16 md:pb-[29px]">
      <a href="/" class="header__logo-link">
        <img src="~/assets/img/logo.svg" alt="Start" class="header__logo-img" />
      </a>
    </h1>
    <!-- md: →  レスポンシブWebデザイン用で768px以上に適用 -->
    <!-- hidden → display: none -->
    <!-- ! →  !important -->
    <button
      class="header__btn-menu hamburger hamburger--slider md:!hidden"
      type="button"
      :class="navOpen ? 'is-active' : ''"
      @click="navOpen = !navOpen"
    >
      <span class="hamburger-box">
        <span class="hamburger-inner"></span>
      </span>
    </button>
    <nav
      class="header__nav fixed right-0 h-screen w-52 bg-[#DD1B57] md:static md:block md:h-auto md:w-auto md:bg-transparent md:pr-16"
      :class="navOpen ? 'block' : 'hidden'"
    >
      <ul class="header__nav-list mt-24 pl-10 md:mt-0 md:flex md:pl-0">
        <li
          class="header__nav-item header__nav-item--active mb-6 font-bold md:mb-0 md:ml-7"
        >
          <a href="/" class="header__nav-link hover:text-[#dd1b57]">ホーム</a>
        </li>
        <li class="header__nav-item mb-6 font-bold md:mb-0 md:ml-7">
          <a href="/message" class="header__nav-link hover:text-[#dd1b57]"
            >メッセージ</a
          >
        </li>
        <li class="header__nav-item mb-6 font-bold md:mb-0 md:ml-7">
          <a href="/company" class="header__nav-link hover:text-[#dd1b57]"
            >会社概要</a
          >
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  // vueファイル内だけで使える変数を作る
  data() {
    return {
      navOpen: false, // false　→　navが閉じている、true　→　navが開いている
    }
  },
}
</script>

<style lang="scss" scoped>
$hamburger-padding-x: 15px !default;
$hamburger-padding-y: 20px !default;
$hamburger-layer-width: 28px !default;
$hamburger-layer-height: 2px !default;
$hamburger-layer-spacing: 6px !default;
$hamburger-layer-color: #fff !default;
$hamburger-layer-border-radius: 2px !default;
$hamburger-hover-opacity: 1 !default;
$hamburger-active-layer-color: $hamburger-layer-color !default;
$hamburger-active-hover-opacity: $hamburger-hover-opacity !default;

// To use CSS filters as the hover effect instead of opacity,
// set $hamburger-hover-use-filter as true and
// change the value of $hamburger-hover-filter accordingly.
$hamburger-hover-use-filter: false !default;
$hamburger-hover-filter: opacity(50%) !default;
$hamburger-active-hover-filter: $hamburger-hover-filter !default;

// Types (Remove or comment out what you don’t need)
$hamburger-types: (slider) !default;
@import 'hamburgers/_sass/hamburgers/hamburgers.scss';

.header {
  &__logo {
    &-link {
    }
    &-img {
      @media (min-width: 768px) {
        width: 167px; /* w167 */
        height: 33px; /* h33 */
      }
    }
  }
  &__nav {
    &-item {
      &--active {
        @media (max-width: 767px) {
          .header__nav-link {
            color: #ef90a4;
          }
        }
        @media (min-width: 768px) {
          .header__nav-link {
            color: #dd1b57;
          }
        }
      }
    }
    &-link {
      @media (max-width: 767px) {
        color: #fff;
      }
    }
  }
  &__btn-menu {
    background-color: #dd1b57;
    border: 1px solid #707070;
    line-height: 1;
    .hamburger-box {
      vertical-align: top;
    }
  }
}
</style>
