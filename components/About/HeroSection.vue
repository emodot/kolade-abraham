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
  background-image: url('assets/images/about_hero.jpg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  display: flex;
  align-items: center;
}

.hero_inner {
  max-width: 1344px;
  width: 40%;
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

.spaned_text {
  color: #B8B8B8;
  font-size: 20px;
}

.wavy {
  text-decoration: underline;
  text-decoration-color: var(--text-color);
  text-decoration-style: wavy;
}
</style>
