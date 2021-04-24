<template>
  <Header />
  <main class="container">
    <router-view />
  </main>
</template>
<script>
import Header from "@/components/Header.vue";
export default {
  components: {
    Header
  }
}
</script>
<style lang="scss">
@import "~@/assets/scss/vars.scss";
@import '~@/assets/scss/styles.scss';
</style>
