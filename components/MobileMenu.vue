<template>
  <div class="mobile_bg">
    <div class="mobile-menu come-down">
    <div class="navbar_inner">
      <div class="logo">
        <img src="~assets/images/KA-logo.png" alt="logo" />
      </div>
      <div class="close" @click="$emit('closeMobileMenu')">
        <span class="bar" />
        <span class="bar2" />
      </div>
    </div>
    <div class="menu-container">
      <nuxt-link to="/" @click="$emit('closeMobileMenu')">
        <p class="menu-text">Home</p>
      </nuxt-link>
      <nuxt-link to="/projects" @click="$emit('closeMobileMenu')">
        <p class="menu-text">Projects</p>
      </nuxt-link>
      <nuxt-link to="/about" @click="$emit('closeMobileMenu')">
        <p class="menu-text">About</p>
      </nuxt-link>
    </div>
    <div class="account_btn">
      <a href="mailto:contact@abrahamkolade.com" target="_blank">
        <button class="global_btn">
          Lets Talk
          <span class="material-icons-outlined arrow_right">
            chevron_right
          </span>
        </button>
      </a>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.mobile_bg {
  position: fixed;
  width: 100%;
  backdrop-filter: blur(10px);
  height: 100%;
  z-index: 15;
}

.mobile-menu {
  /* position: fixed; */
  z-index: 15;
  background-color: #000;
  width: 100%;
  padding-bottom: 20px;
}

.navbar_inner {
  max-width: 1344px;
  height: 120px;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 80%;
}

.logo {
  /* margin-right: 5rem; */
  width: 12%;
}

.logo img {
  cursor: pointer;
  width: 100%;
}

.close {
  color: #fff;
  cursor: pointer;
}

.bar,
.bar2 {
  display: block;
  width: 22px;
  height: 2px;
  margin: 5px auto;
  background-color: #fff;
  cursor: pointer;
}

.bar {
  transform: rotate(45deg);
  position: absolute;
}

.bar2 {
  transform: rotate(-45deg);
}

.menu-container {
  display: flex;
  flex-direction: column;
  font-size: 16px;
  width: 100%;
}

.menu-text {
  padding: 30px 50px;
  color: #fff;
  text-align: center;
}

.account_btn {
  width: fit-content;
  margin: 30px auto;
}

.global_btn {
  color: white;
  border: 1px solid #fff;
  display: flex;
  align-items: center;
}
.arrow_right {
  color: #fff;
  margin-left: 6px;
}

@media only screen and (max-width: 500px) {
  .logo {
    width: 14%;
  }
  .navbar_inner {
    width: 85%;
  }
  .menu-text {
    padding: 20px 20px;
  }
}
</style>
