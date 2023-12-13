<script>
import PageHeader from "./components/PageHeader.vue"
import PageMain from "./components/PageMain.vue"
import PageFooter from "./components/PageFooter.vue"
import { store } from "./store.js"

export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter
  },
  data() {
    return {
      store           //importo lo store in data
    }
  },
  methods: {},
  mounted: function () {

  }
}
</script>

<template>
  <main>
    <PageHeader class="header" :menu="store.menulist"></PageHeader>
    <PageMain></PageMain>
  </main>
  <PageFooter class="footer"></PageFooter>
</template>


<style lang="scss">
@use './styles/general.scss';
</style>

<style scoped lang="scss">
@use "./styles/partials/_variables.scss" as *;

main {
  position: relative;
  min-height: 100vh;
  width: 100vw;
  margin-bottom: $footer_height;
  z-index: 2;
}

/// footer che scorre preso da https://stackoverflow.com/questions/46399312/vuejs-footer-with-scroll-reveal
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  z-index: 0;
}
</style>
