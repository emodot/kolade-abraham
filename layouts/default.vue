<template>
  <div class="main">
    <Navbar
      @triggerMobileMenu="showMobileMenu = true"
    />
    <div class="mobile-menu">
      <MobileMenu
        v-show="showMobileMenu"
        @closeMobileMenu="showMobileMenu = false"
      />
    </div>
    <div class="main_content">
      <slot />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  data () {
    return {
      showMobileMenu: true
    }
  },

}
</script>

<style scoped>
.main {
  background-color: #000;
}

</style>
