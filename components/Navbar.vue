<template>
  <div
    class="navbar_ctn"
    :class="{ 'blurry-bg': scrolled }"
    @scroll.passive="handleScroll"
  >
    <div class="navbar_inner">
      <div class="navbar_lhs">
        <div class="logo">
          <img
            :src="`${scrolled ? '/KA-logo-black.png' : '/KA-logo.png'}`"
            alt=""
            @click="$router.push('/')"
          />
        </div>
      </div>
      <div class="navbar_rhs">
        <div class="menu_list">
          <nuxt-link to="/">
            <p class="menu_item" :class="{ 'color-black': scrolled }">Home</p>
          </nuxt-link>
          <nuxt-link to="#projects">
            <p class="menu_item" :class="{ 'color-black': scrolled }">
              Projects
            </p>
          </nuxt-link>
          <nuxt-link to="/about">
            <p class="menu_item" :class="{ 'color-black': scrolled }">About</p>
          </nuxt-link>
          <div class="account_btn">
            <a href="mailto:contact@abrahamkolade.com" target="_blank">
              <button class="global_btn" :class="{ 'btn-black': scrolled }">
                Lets Talk
                <span class="material-icons-outlined arrow_right">
                  chevron_right
                </span>
              </button>
            </a>
          </div>
        </div>
        <div class="mobile_menu">
          <svg
            class="hamburger"
            @click="$emit('triggerMobileMenu')"
            width="20"
            height="11"
            viewBox="0 0 20 11"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1 1H10.9"
              :stroke="`${scrolled ? '#000' : '#F9F8F8'}`"
              stroke-width="2"
              stroke-linecap="round"
            />
            <path
              d="M1 5.5H19"
              :stroke="`${scrolled ? '#000' : '#F9F8F8'}`"
              stroke-width="2"
              stroke-linecap="round"
            />
            <path
              d="M9.1001 10H19.0001"
              :stroke="`${scrolled ? '#000' : '#F9F8F8'}`"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const scrolled = ref(false);

function handleScroll() {
  scrolled.value = window.scrollY > 0;
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});
</script>

<style scoped>
.navbar_ctn {
  background-color: transparent;
  position: fixed;
  width: 100%;
  z-index: 5;
  transition: backdrop-filter 0.3s;
  backdrop-filter: blur(0px);
}
.navbar_ctn.blurry-bg {
  backdrop-filter: blur(10px);
  background-color: rgba(255, 255, 255, 0.5);
}
.navbar_inner {
  max-width: 1344px;
  width: 70%;
  height: 120px;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.color-black {
  color: #000 !important;
}
.btn-black {
  border: 1px solid #000 !important;
  color: #000 !important;
}
.btn-black .arrow_right {
  color: #000;
}

.navbar_lhs {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-basis: 20%;
}

.logo {
  /* margin-right: 5rem; */
  width: 30%;
}

.logo img {
  cursor: pointer;
  width: 100%;
}

.navbar_rhs {
  height: 100%;
  flex-basis: 75%;
  display: flex;
  justify-content: flex-end;
}

.menu_list {
  display: flex;
  align-items: center;
  width: 60%;
  justify-content: space-between;
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

.menu_item {
  cursor: pointer;
  color: #fff;
  font-weight: 500;
}

.account_btn {
  cursor: pointer;
  display: flex;
  align-items: center;
  /* margin-left: 30px; */
}

.mobile_menu {
  height: 100%;
  display: none;
  padding-left: 20px;
  margin-left: 20px;
  border-left: 1px solid var(--border-color);
}

.hamburger {
  cursor: pointer;
  width: 24px;
}

@media only screen and (max-width: 1200px) {
  /* .navbar_lhs {
    flex-basis: 30%;
  } */
  .navbar_inner {
    width: 85%;
  }
  .logo {
    width: 40%;
  }
  .menu_list {
    width: 80%;
  }
}
@media only screen and (max-width: 900px) {
  .logo {
    width: 60%;
  }
  .navbar_inner {
    width: 80%;
  }
  .menu_list {
    display: none;
  }
  .mobile_menu {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
@media only screen and (max-width: 500px) {
  .logo {
    width: 40%;
  }
  .navbar_inner {
    width: 85%;
  }
  .navbar_lhs {
    flex-basis: 40%;
  }
  .account_btn {
    display: none;
  }
}
</style>
