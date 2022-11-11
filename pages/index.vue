<template>
  <div class="font-noto">
    <!--
      flex-col: flex-direction: column; 子要素を縦並びにする
      items-center: align-items: center; 縦並びのときは横方向のセンター揃え
      justify-center: justify-content: center; 縦並びのときは縦方向のセンター揃え
     -->
    <div
      class="mv flex h-[460px] flex-col items-center justify-center text-white md:h-[600px]"
    >
      <h1 class="mv__title mb-2.5 text-7xl font-bold md:text-[160px]">START</h1>
      <p class="mv__catch text-xl font-medium md:text-2xl">
        仕事に最高のスタートを。
      </p>
    </div>
    <section class="sec-news">
      <h2 class="sec-news__heading">ニュース</h2>
      <dl class="sec-news__list">
        <!-- ===== -->
        <div
          class="sec-news__item"
          v-for="newsContent in newsContents"
          :key="newsContent.title"
        >
          <dt class="sec-news__date">{{ newsContent.date }}</dt>
          <dd class="sec-news__title">{{ newsContent.title }}</dd>
        </div>
        <!-- ===== -->
      </dl>
    </section>
    <!-- /.sec-news -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      newsContents: [
        {
          date: '2023.02.10',
          title: 'コーポレートサイトをリニューアルしました。',
        },
        {
          date: '2023.02.08',
          title: '採用を強化中です！一緒に働きませんか？',
        },
        {
          date: '2022.02.02',
          title:
            '人材紹介SNS『スタート』をリリースしました。3/31まで新規登録キャンペーンを開催中です！サービス内で使える500ポイントをプレゼント！',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.mv {
  background: url(~/assets/img/bg_mv_sp.png) no-repeat 0 0;
  background-size: cover;
  @media (min-width: 768px) {
    background-image: url(~/assets/img/bg_mv_pc.png);
  }
  &__title {
  }
  &__catch {
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
