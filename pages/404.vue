<template>
  <div class="hero_ctn">
    <div class="hero_inner">
      <img src="assets/images/2.webp" alt="" />
      <h1 class="hero_head">
        Oops<span class="spanned_text">, Almost done</span>!
      </h1>
      <p class="hero_text">
        This project’s information is all-over-the-place. <br />I am working
        hard to present it beautifully and will update it soon.
      </p>
      <div class="btns">
        <a href="https://dribbble.com/Kola_abr" target="_blank">
          <button class="global_btn">
            <span class="spanned_text">Checkout</span> My dribbble
          </button>
        </a>
        <button class="global_btn btn_2" @click="navigateTo('/')">
          Back to Home
          <span class="material-icons-outlined arrow_right">
            chevron_right
          </span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "error",
});
useHead(() => ({
  status: 404,
  title: "Page not found",
}));
</script>

<style scoped>
.hero_ctn {
  height: 80vh;
  background-color: #000;
  display: flex;
  align-items: center;
}

.hero_inner {
  max-width: 1344px;
  width: 45%;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

img {
  text-align: center;
  margin: auto;
  margin-bottom: 40px;
  width: 30%;
}

.hero_head {
  color: #fff;
  font-family: Power Grotesk;
  font-size: 56px;
  font-style: normal;
  font-weight: 500;
  text-align: center;
}

.spanned_text {
  color: inherit;
  font-family: inherit;
  font-size: inherit;
  font-weight: inherit;
}

.hero_text {
  color: var(--text-color);
  font-size: 18px;
  margin-top: 15px;
  text-align: center;
  line-height: 26px;
}

.btns {
  display: flex;
  margin-top: 40px;
}

.global_btn {
  color: white;
  border: 1px solid #fff;
  display: flex;
  align-items: center;
  height: 40px;
  margin: 0 10px;
}

.btn_2 {
  background-color: #fff;
  color: #0c0c0c;
}

.arrow_right {
  color: #0c0c0c;
  margin-left: 6px;
}

@media only screen and (max-width: 900px) {
  .hero_inner {
    width: 85%;
  }
}

@media only screen and (max-width: 500px) {
  .spanned_text {
    display: none;
  }
  img {
    width: 50%;
  }
  .hero_head {
    font-size: 40px;
  }
  .hero_text {
    font-size: 14px;
  }
}
</style>
