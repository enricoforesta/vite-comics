<script>
import AppComponentNav from './components/ComponentHeader/AppComponentNav.vue';
import AppComponentContent from './components/ComponentHeader/AppComponentContent.vue';
import AppComponentBuy from './components/ComponetnMain/AppComponentBuy.vue';
import AppComponentMainBottom from './components/ComponetnMain/AppComponentMainBottom.vue';
import AppComponentFooter from './components/ComponentFooter/AppComponentFooter.vue';
export default {
  name: "APP",
  components: {
    AppComponentNav,
    AppComponentContent,
    AppComponentBuy,
    AppComponentMainBottom,
    AppComponentFooter
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
  <footer>
    <AppComponentFooter />
  </footer>
</template>

<style lang="scss">
@use'./style/general.scss' as *;
</style>
