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
  <div class="container">
    <AppHeader />
    <AppMain />
    <AppFooter />
  </div>
</template>

<style lang="scss">
@import "src/styles/general.scss";
</style>
