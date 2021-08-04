<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">{{ $t('companyName') }}</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item><nuxt-link :to="'/'">{{ $t('Home') }}</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link :to="'/subscribers'">{{ $t('Subscribers') }}</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link :to="'/partners'">{{ $t('Partners') }}</nuxt-link></b-nav-item>
          <b-nav-item><nuxt-link :to="'/reports'">{{ $t('Reports') }}</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>

</style>
