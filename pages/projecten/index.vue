<template>
  <div>
    <header>
      <div class="img-container">
        <b-img-lazy src="~/assets/images/hero.jpg"></b-img-lazy>
        <h1 class="text-center header-title">Projecten</h1>
      </div>
    </header>

    <b-container class="bv-example-row" fluid>
      <date-picker />
      <add-to-cart-animation />
      <dynamic-hover-menu />
    </b-container>
  </div>
</template>

<script>
import AddToCartAnimation from '~/components/projectpage/AddToCartAnimation.vue'
import datePicker from '~/components/projectpage/DatePicker.vue'
import DynamicHoverMenu from '~/components/projectpage/DynamicHoverMenu.vue'
export default {
  name: 'Page1',
  components: { datePicker, AddToCartAnimation, DynamicHoverMenu },
  data() {
    return {
      slide: 0,
      sliding: null,
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
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
.white-bg {
  background-color: $color-white;
}
.black-bg {
  background-color: $color-black;
  color: $color-white;
}
</style>
