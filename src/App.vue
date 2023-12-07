<script>
import AppComponentNav from './components/ComponentHeader/AppComponentNav.vue';
import AppComponentContent from './components/ComponentHeader/AppComponentContent.vue';
export default {
  name: "APP",
  components: {
    AppComponentNav,
    AppComponentContent,

  }
}
</script>

<template>
  <header>
    <AppComponentNav />
    <AppComponentContent />
  </header>
</template>

<style lang="scss">
@use'./style/general.scss' as *;
</style>
