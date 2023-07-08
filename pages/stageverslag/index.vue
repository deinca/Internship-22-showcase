<template>
  <div>
    <header class="mb-5">
      <div class="img-container">
        <b-img-lazy src="~/assets/images/hero.jpg"></b-img-lazy>
        <h1 class="text-center header-title">Stageverslag</h1>
      </div>
    </header>
    <b-container class="mb-5">
      <embed
        src="https://drive.google.com/file/d/1ztsgmsYlANyl9JF2Irqayhtx5mevVOaY/preview"
        width="100%"
        height="600px"
      />
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'Page1',
}
</script>
<style lang="scss" scoped>
header img {
  width: 100%;
  display: flex;
  object-fit: cover;
  object-position: bottom;
}
.img-container {
  height: 12rem;
  overflow: hidden;
  width: inherit;
  display: flex;
  justify-content: center;
}
.header-title {
  position: absolute;
  align-self: center;
  color: $color-white;
}
</style>
