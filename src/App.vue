<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: "App",
  components: {
    AppHeader,
    AppContent,
    AppFooter,
  }

}
</script>

<template>
  <AppHeader />
  <AppContent/>
  <AppFooter/>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
</style>
