<template>
  <div class="font-noto">
    <h1>Title</h1>
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
