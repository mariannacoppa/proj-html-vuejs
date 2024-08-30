<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>
<template>
  <div>
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
  <!-- <h1>Getting Started with Vue.js and Font Awesome</h1>
  <p>Have a phone call: <font-awesome-icon icon="phone" /></p>
  <font-awesome-icon icon="envelope" />
  <font-awesome-icon icon="location-dot" />
  <font-awesome-icon icon="magnifying-glass" />
  <font-awesome-icon icon="quote-left" />
  <font-awesome-icon icon="instagram" /> -->
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>