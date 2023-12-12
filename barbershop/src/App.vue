<script>
import PageHeader from "./components/PageHeader.vue"
import { store } from "./store.js"

export default {
  components: {
    PageHeader
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
  </main>
</template>


<style lang="scss">
@use './styles/general.scss';
</style>

<style scoped lang="scss">
main {
  position: relative;
  height: 100vh;
  width: 100vw;
}

.header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
}
</style>
