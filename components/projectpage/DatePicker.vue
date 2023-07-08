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
          background="#ababab"
          style="text-shadow: 1px 1px 2px #333"
          @sliding-start="onSlideStart"
          @sliding-end="onSlideEnd"
        >
          <b-carousel-slide
            img-src="~/assets/images/date-picker.png"
          ></b-carousel-slide>
        </b-carousel>
      </b-col>
      <b-col align-self="center" cols="4">
        <h2>Date Picker</h2>
        <p>
          Bij deze opdracht ben ik begonnen te werken als een Front-End
          developer door te leren werken met de JavaScript framework Vue en
          Nuxt.
        </p>
        <p>
          Mijn oplossing was om een NPM package (een JavaScript programma pakket
          die een developer kan gebruiken in zijn projecten) te installeren en
          toe te passen aan het project. Binnen dit programma had ik de
          mogelijkheid om allerlei functionaliteiten aan te passen aan de
          kalender en zo de opdracht te kunnen oplossen.
        </p>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'DatePicker',
}
</script>
<style lang="scss" scoped>
.white-bg {
  background-color: $color-white;
}
</style>
