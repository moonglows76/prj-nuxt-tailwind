<template>
  <div class="header flex justify-between font-noto">
    <h1 class="header__logo pt-5 pl-5 pb-[19px]">
      <a href="/" class="header__logo-link">
        <img src="~/assets/img/logo.svg" alt="Start" />
      </a>
    </h1>
    <button
      class="header__btn-menu hamburger hamburger--slider md:!hidden"
      type="button"
    >
      <span class="hamburger-box">
        <span class="hamburger-inner"></span>
      </span>
    </button>
    <nav class="header__nav hidden md:block">
      <ul class="header__nav-list">
        <li class="header__nav-item">
          <a href="/" class="header__nav-link">ホーム</a>
        </li>
        <li class="header__nav-item">
          <a href="/message" class="header__nav-link">メッセージ</a>
        </li>
        <li class="header__nav-item">
          <a href="/company" class="header__nav-link">会社概要</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
$hamburger-padding-x: 15px !default;
$hamburger-padding-y: 20px !default;
$hamburger-layer-width: 28px !default;
$hamburger-layer-height: 2px !default;
$hamburger-layer-spacing: 6px !default;
$hamburger-layer-color: #fff !default;
$hamburger-layer-border-radius: 2px !default;
$hamburger-hover-opacity: 0.7 !default;
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
  color: red;
  &__logo {
    &-link {
      color: blue;
    }
  }
  &__nav {
    &-link {
      color: green;
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
