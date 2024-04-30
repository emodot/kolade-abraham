<template>
  <div class="hero_ctn">
    <div class="hero_inner">
      <h1 class="hero_head">Yep, that’s me!</h1>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.hero_ctn {
  height: 80vh;
  background-image: url("assets/images/about_hero.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  display: flex;
  align-items: center;
}

.hero_inner {
  max-width: 1344px;
  /* width: 40%; */
  margin: auto;
}

.hero_head {
  color: #fff;
  font-family: Power Grotesk;
  font-size: 54px;
  font-style: normal;
  font-weight: 500;
}

.hero_text {
  color: var(--text-color);
  font-size: 20px;
  margin-top: 15px;
}

@media only screen and (max-width: 1200px) {
  .hero_ctn {
    height: 80vh;
  }
  .hero_head {
    font-size: 45px;
  }
}

@media only screen and (max-width: 500px) {
  .hero_inner {
    width: 100%;
    position: relative;
    height: 100%;
  }
  .hero_head {
    position: absolute;
    left: 20px;
    bottom: 30px;
  }
}
</style>
