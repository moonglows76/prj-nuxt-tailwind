<template>
  <div class="container mx-auto px-4">
    <div class="header">
      header
      <div class="header__logo">header__logo</div>
    </div>

    <h2>Grid</h2>
    <div class="row-grid grid">
      <div>1 2 3 4 5 6 7 8 9 0</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
      <div>6</div>
    </div>

    <h2>Flexbox</h2>
    <div class="flex flex-wrap">
      <div class="shrink grow basis-24">1 2 3 4 5 6 7 8 9 0</div>
      <div class="shrink grow basis-24">2</div>
      <div class="shrink grow basis-24">3</div>
      <div class="shrink grow basis-24">4</div>
      <div class="shrink grow basis-24">5</div>
      <div class="shrink grow basis-24">6</div>
    </div>

    <h2>min()</h2>
    <div class="img-min">
      <img src="https://placeimg.com/640/480/animals" alt="" />
    </div>
    <h2>max()</h2>
    <div class="img-max">
      <img src="https://placeimg.com/640/480/animals" alt="" />
    </div>

    <h2>clamp()</h2>
    <div class="img-clamp">
      <img src="https://placeimg.com/640/480/animals" alt="" />
    </div>

    <p>
      いろはにほへと　ちりぬるを わかよたれそ　つねならむ
      うゐのおくやま　けふこえて あさきゆめみし　ゑひもせす
      色は匂へど　散りぬるを 我が世誰ぞ　常ならむ 有為の奥山　今日越えて
      浅き夢見じ　酔ひもせず
    </p>

    <h2>calc()</h2>
    <div class="img-calc">
      <img src="https://placeimg.com/640/480/animals" alt="" />
    </div>

    <h2>vw</h2>
    <div class="img-vw">
      <img src="https://placeimg.com/640/480/animals" alt="" />
    </div>

    <h2>aspect-ratio</h2>
    <div class="img-aspect-ratio">
      <img
        src="https://placeimg.com/640/480/animals"
        alt=""
        class="aspect-square object-cover object-center"
      />
    </div>

    <h1
      class="heading-lv1 mt-12 mb-7 ml-2.5 text-3xl font-normal leading-relaxed"
    >
      シナプスぶろぐとは
    </h1>
    <h1 class=""></h1>
    <h2
      class="heading-lv2 relative mt-12 mb-7 bg-teal-100 pt-1 pr-2.5 pl-7 pb-1 text-2xl font-normal leading-relaxed text-teal-900 before:absolute before:top-2 before:left-2 before:block before:h-7 before:w-1 before:bg-teal-600"
    >
      シナプスぶろぐ更新情報
    </h2>
    <div class="mt-5">
      <input
        type="submit"
        value="ログイン"
        class="btn-submit box-border block w-full cursor-pointer appearance-none rounded border border-teal-900 bg-teal-200 py-2.5 text-center text-lg leading-none text-teal-700 shadow-md"
      />
    </div>
  </div>
</template>
<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss" scoped>
.header {
  color: red;
  &__logo {
    color: blue;
  }
}
.row-grid {
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
}

.row-flex div {
  flex: 1 1 100px;
}

.img-min {
  width: min(50%, 500px);
}
.img-max {
  width: max(50%, 500px);
}
.img-clamp {
  width: clamp(200px, 100%, 50%);
}
p {
  font-size: clamp(1rem, 2.5vw, 2rem);
}
.img-calc {
  width: calc(100% / 3);
}
.img-vw {
  width: 33.3vw;
}

.img-aspect-ratio img {
  width: 300px;
}
</style>
