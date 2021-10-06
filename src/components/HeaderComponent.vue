<template id="header">
  <w-flex class="noshrink">
    <h1 class="xs10 headline ma3 pa1 text-center text-bold">Awesome Airlines</h1>
    <w-button @click="showDrawer = true" bg-color="indigo-dark2" xl>
      <w-icon color="white" class="xs2 ma3 pa1">mdi mdi-menu</w-icon>
    </w-button>
    <w-icon></w-icon>
  </w-flex>
  <w-drawer v-model="showDrawer" right width="350px">
    <w-button
      class="button--close"
      @click="showDrawer = false"
      sm
      outline
      round
      absolute
      color="primary"
      icon="wi-cross"
    ></w-button>
    <nav-accordion></nav-accordion>
  </w-drawer>
</template>

<script>
import NavAccordion from './NavAccordion.vue'

export default {
  name: 'HeaderComponent',
  data: () => ({
    showDrawer: false
  }),
  components: {
    'nav-accordion': NavAccordion
  }
}
</script>

<style scoped>
#header {
  margin-top: 10px;
  position: relative;
  overflow: hidden;
}

@media only screen and (max-width: 600px) {
  header {
    height: 135px;
  }
}

@media screen and (min-width: 601px) and (max-width: 1200px) {
  header {
    height: 180px;
  }
}
</style>