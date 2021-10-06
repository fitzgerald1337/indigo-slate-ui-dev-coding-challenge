The App component.

  - Contains the basic WaveUI app structure
  - Provides basic HTML5 semantic structure for better accessibility

<template>
  <w-app id="app" class="w-flex row">
    <w-flex column>
      <header>
        <header-component />
      </header>
      <main class="grow">
        <main-content />
      </main>
      <footer>
        <footer-component />
      </footer>
    </w-flex>
  </w-app>

  <!--
    template for other screen layouts -> trouble implementing with Vue dynamic components 

    <w-app id="app" class="w-flex row">
    <aside>Nav menu</aside>
    <w-flex column>
      <header>Header</header>
      <main class="grow">Main content</main>
      <footer>Footer</footer>
    </w-flex>
  </w-app> -->

</template>



<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainContent from './components/MainContent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    'header-component': HeaderComponent,
    'main-content': MainContent,
    'footer-component': FooterComponent
  }
}
</script>

<style scoped>
#app {
  background-color: rgba(3, 3, 75, 0.952);
  color: white;
}
</style>
