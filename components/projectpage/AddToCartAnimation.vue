<template>
  <div>
    <b-row class="pb-5 pt-5 black-bg">
      <b-col align-self="center" cols="4">
        <h2>Add to cart Animation</h2>
        <p>
          Bij deze opdracht heb ik de code gemaakt om het volgende states
          mogelijk te maken.
        </p>
        <p>
          <b>Empty cart state:</b> Als er geen producten zijn gezet in de
          winkelwagen, laat dan een empty sate zien.
        </p>
        <p>
          <b>Product added state:</b> Als er een producten is toegevoegd in de
          winkelwagen, blaas dan een groen ballon zien.
        </p>
        <p>
          <b>Product removed state:</b> Als en producten wordt verwijderd, laat
          dan een rode ballon zien.
        </p>
        <p>
          <b>Products in cart state:</b>
          Nadat de groen/rood ballon is weergegeven of de webpagina herstart,
          zet na een 0.8 seconde de ballon op orange. Zodat de gebruiker weet
          dat er nog producten in de winkelwagen zitten.
        </p>
        <p>
          <b>Return to Empty cart state: </b>
          Als alle producten zijn verwijderd, verander het ballon van orange
          naar rood en blaas deze uit. Laat daarna de Empty cart sate zien.
        </p>
      </b-col>

      <b-col>
        <b-carousel
          id="carousel-1"
          v-model="slide"
          :interval="4000"
          controls
          indicators
          background="#ababab"
          img-width="1024"
          img-height="480"
          style="text-shadow: 1px 1px 2px #333"
          @sliding-start="onSlideStart"
          @sliding-end="onSlideEnd"
        >
          <b-carousel-slide
            img-src="~/assets/images/add-to-cart-aniamtion.gif"
          ></b-carousel-slide>
        </b-carousel>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'AddToCartAnimation',
}
</script>

<style lang="scss" scoped>
.black-bg {
  background-color: $color-black;
  color: $color-white;
}
</style>
