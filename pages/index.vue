<template>
  <div>
    <header class="mb-5">
      <div class="img-container">
        <b-img-lazy src="~/assets/images/hero.jpg"></b-img-lazy>
        <h1 class="text-center header-title">Homepage</h1>
      </div>
    </header>

    <b-container class="mb-5">
      <b-row cols="12" align-v="stretch">
        <b-col sm="4"><home-projecten /></b-col>
        <b-col sm="4"><home-stageverslag /></b-col>
        <b-col sm="4"><home-contact /></b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import HomeProjecten from '~/components/homepage/HomeProjecten.vue'
import HomeContact from '~/components/homepage/HomeContact.vue'
import HomeStageverslag from '~/components/homepage/HomeStageverslag.vue'
export default {
  name: 'Homepage',
  components: { HomeProjecten, HomeStageverslag, HomeContact },
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
