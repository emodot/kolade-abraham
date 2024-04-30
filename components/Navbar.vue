<template>
  <div class="navbar_ctn">
    <div class="navbar_inner">
      <div class="navbar_lhs">
        <div class="logo">
          <img
            src="~assets/images/KA-logo.png"
            alt=""
            @click="$router.push('/')"
          />
        </div>
      </div>
      <div class="navbar_rhs">
        <div class="menu_list">
          <nuxt-link to="/">
            <p class="menu_item">Home</p>
          </nuxt-link>
          <nuxt-link to="#">
            <p class="menu_item">Projects</p>
          </nuxt-link>
          <nuxt-link to="/about">
            <p class="menu_item">About</p>
          </nuxt-link>
          <div class="account_btn">
            <button class="global_btn">
              My Account
              <span class="material-icons-outlined arrow_right">
                chevron_right
              </span>
            </button>
          </div>
        </div>
        <div class="mobile_menu">
          <img
            class="hamburger"
            src="assets/icons/hamburger.svg"
            alt=""
            @click="$emit('triggerMobileMenu')"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const isSticky = ref(false);
const productList = ref({});

// onMounted(() => {
//   console.log("the component is created");
//   window.addEventListener("scroll", this.makeHeaderSticky);
// });
// onBeforeUnmount(() => {
//   console.log("the component is destroyed");
//   window.removeEventListener("scroll", this.makeHeaderSticky);
// });

// const makeHeaderSticky = () => {
//   if (window.scrollY > 0) {
//     isSticky.value = true;
//   } else {
//     isSticky.value = false;
//   }
//   console.log(isSticky.value);
// };
</script>

<style scoped>
.navbar_ctn {
  background-color: transparent;
  /* box-shadow: 0px 5px 20px #dadada; */
  position: fixed;
  width: 100%;
  z-index: 5;
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
