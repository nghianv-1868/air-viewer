<template>
  <div id="wrapper" class="d-flex flex-column">
    <header class="header-global">
      <starter-header />
    </header>
    <div class="">
      <nuxt />
    </div>
    <footer class="footer">
      <starter-footer />
    </footer>
  </div>
</template>

<script>
import StarterHeader from '~/components/argon-layout/AppHeader'
import StarterFooter from '~/components/argon-layout/AppFooter'

export default {
  components: {
    StarterHeader,
    StarterFooter
  }
}
</script>

<style>
body, #wrapper {
   min-height:100vh;
}
</style>
