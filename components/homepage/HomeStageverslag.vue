<template>
  <div>
    <h2>Stageverslag</h2>
    <b-card no-body img-top class="mb-3">
      <div class="img-container">
        <b-img-lazy
          src="https://images.unsplash.com/photo-1470790376778-a9fbc86d70e2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1904&q=80"
        ></b-img-lazy>
      </div>
    </b-card>
    <b-button pill href="/stageverslag" class="button-blue p-3 w-100"
      >Bekijken</b-button
    >
  </div>
</template>

<script>
export default {
  name: 'HomeStageverslag',
}
</script>
<style lang="scss" scoped>
.img-container {
  height: 32rem;
  overflow: hidden;
  width: inherit;
  display: flex;
  justify-content: center;
}
.img-container img {
  position: relative;
  height: inherit;
}
h1 {
  color: $color-primary;
}
.button-blue {
  background-color: $color-midnight-blue;
  border: none;
}
.button-blue:hover {
  background-color: $color-cerulean;
}
</style>
