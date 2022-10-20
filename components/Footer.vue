<template>
  <div class="footer px-5 pb-7 font-noto">
    <div class="footer__inner">
      <ul class="footer__nav-list flex gap-x-6">
        <li class="footer__nav-item font-bold">
          <a href="/" class="footer__nav-link text-white">ホーム</a>
        </li>
        <li class="footer__nav-item font-bold">
          <a href="/message" class="footer__nav-link text-white">メッセージ</a>
        </li>
        <li class="footer__nav-item font-bold">
          <a href="/company" class="footer__nav-link text-white">会社概要</a>
        </li>
      </ul>
      <p class="footer__copyright mt-5">
        <small class="footer__copyright-small text-white">© START</small>
      </p>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.footer {
  background-color: #dd1b57;
  padding-top: clamp(
    2.5rem,
    2.0598591549295775rem + 1.8779342723004695vw,
    3.75rem
  );
  &__inner {
    max-width: 1110px;
    margin: 0 auto;
  }
  &__nav-list {
    font-size: clamp(
      0.75rem,
      0.7059859154929577rem + 0.18779342723004694vw,
      0.875rem
    );
  }
  &__copyright {
    &-small {
      font-size: clamp(
        0.625rem,
        0.5809859154929577rem + 0.18779342723004694vw,
        0.75rem
      );
    }
  }
}
</style>
