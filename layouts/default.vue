<template>
  <div class="page-container grid h-screen grid-rows-[auto_1fr_auto]">
    <Header /><!-- components/Header.vueが入ってくる -->
    <nuxt /><!-- pages/*.vue が入ってくる -->
    <Footer /><!-- components/Footer.vueが入ってくる -->
  </div>
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
.page-container {
  /* grid-template-rows: auto 1fr auto;の指定がtailwindcssになければここに書く */
  // flex: 1 0 100px;
  // ↓ 同じ
  // flex-grow: 1;  //領域が余ったら大きくする比率
  // flex-shrink: 0;  //領域が余ってないときに小さくする比率
  // flex-basis: 100px;  //基準の幅
}
</style>
