<template id="footer">
  <w-drawer
    v-model="showCookieNotice"
    content-class="cookie-notice"
    overlay-color="transparent"
    persistent
    fit-content
    bottom
  >
    <div class="w-flex ma5 pa5 align-center wrap">
      <div class="w-flex align-center">
        <w-icon class="mr3" color="indigo-light1" xl>wi-info-circle</w-icon>
        <span class="grey-dark3">
          Our website uses cookies to give you the best user experience.
          To continue browsing this site you must agree.
        </span>
      </div>
      <div class="spacer" />
      <w-button
        class="w-flex align-right wrap ma3"
        sm
        bg-color="indigo-light1"
        dark
        @click="showCookieNotice = false"
      >
        <w-icon class="mr2">mdi mdi-cookie</w-icon>I agree!
      </w-button>
    </div>
  </w-drawer>
  <h6
    class="caption text-center white pa5 ma3"
  >Created by Michael Fitzgerald for Indigo Slate's UI Developer coding challenge, October 2021.</h6>
</template>

<script>
export default {
  data: () => ({
    showCookieNotice: true
  })
}
</script>

<style scoped>
#footer {
  height: 20%;
}
</style>
