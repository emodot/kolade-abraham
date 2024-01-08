<template>
  <div class="main">
    <Navbar
      @open-cart="openCart = true"
      @showMobileMenu="showMobileMenu = true"
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
      openCart: false,
      showMobileMenu: false
    }
  },
  methods: {
  }

}
</script>

<style scoped>
.main {
  background-color: #ffffff;
}

</style>
