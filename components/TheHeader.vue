<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand to="/">Deivers Wavin Showcase</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/projecten">Projecten</b-nav-item>
          <b-nav-item to="/stageverslag">Stageverslag</b-nav-item>
          <b-nav-item to="/contact">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'TheHeader',
}
</script>
<style lang="scss" scoped>
nav {
  background: $color-tory-blue;
  padding: 1rem 1.5rem;
}
h1 {
  color: $color-primary;
}
</style>
