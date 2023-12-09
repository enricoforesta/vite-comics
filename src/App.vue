<script>
import AppComponentNav from './components/ComponentHeader/AppComponentNav.vue';
import AppComponentContent from './components/ComponentHeader/AppComponentContent.vue';
import AppComponentBuy from './components/ComponetnMain/AppComponentBuy.vue';
import AppComponentMainBottom from './components/ComponetnMain/AppComponentMainBottom.vue';
export default {
  name: "APP",
  components: {
    AppComponentNav,
    AppComponentContent,
    AppComponentBuy,
    AppComponentMainBottom,
  }
}
</script>

<template>
  <header>
    <AppComponentNav />
    <AppComponentContent />
  </header>
  <main>
    <AppComponentBuy />
    <AppComponentMainBottom />
  </main>
</template>

<style lang="scss">
@use'./style/general.scss' as *;
</style>
