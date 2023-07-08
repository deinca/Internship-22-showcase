<template>
  <div>
    <b-row class="pb-5 pt-5 white-bg">
      <b-col>
        <b-carousel
          id="carousel-1"
          v-model="slide"
          :interval="4000"
          controls
          indicators
          background="#fff"
          img-height="400"
          style="text-shadow: 1px 1px 2px #333"
          @sliding-start="onSlideStart"
          @sliding-end="onSlideEnd"
        >
          <b-carousel-slide
            img-src="~/assets/images/dhm-1.jpg"
          ></b-carousel-slide>
          <b-carousel-slide
            img-height="800"
            img-src="~/assets/images/dhm-2.jpg"
          ></b-carousel-slide>
          <b-carousel-slide
            img-height="800"
            img-src="~/assets/images/dhm-3.jpg"
          ></b-carousel-slide>
          <b-carousel-slide
            img-height="800"
            img-src="~/assets/images/dhm-4.jpg"
          ></b-carousel-slide>
        </b-carousel>
      </b-col>

      <b-col align-self="center" cols="4">
        <h2>Dynamic hover menu</h2>
        <p>
          Bij deze opdracht was de taak om de menu buttons van de Wavin
          e-commerce site dynamisch te maken. Dit betekende dat ik
          verantwoordelijk was voor de functie dat als je met de muis op de
          button/link staat dat je een title te zien krijgt die opgehaald wordt
          vanuit de content management systeem. Deze functionaliteit moest ik
          met JavaScript programmeren.
        </p>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'DynamicHoverMenu',
}
</script>

<style lang="scss" scoped>
.white-bg {
  background-color: $color-white;
}
</style>
