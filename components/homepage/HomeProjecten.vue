<template>
  <div>
    <h2>Projecten</h2>
    <b-card no-body img-top class="mb-3">
      <!-- <b-skeleton-img card-img="top" aspect="3:5"></b-skeleton-img> -->
      <div class="img-container">
        <b-img-lazy
          src="https://images.unsplash.com/photo-1608760000795-547e78bfc003?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=450&q=80"
        ></b-img-lazy>
      </div>
    </b-card>
    <b-button pill href="/projecten" class="button-blue p-3 w-100"
      >Bekijken</b-button
    >
  </div>
</template>

<script>
export default {
  name: 'HomeProjecten',
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
