<template>
  <div class="hero_ctn">
    <div class="hero_inner">
      <h1 class="hero_head">Hello,</h1>
      <p class="hero_text">
        I am ‘Kola, I like to make digital experiences <span class="spaned_text wavy">easier and simpler</span> for
        people.
      </p>
      <p class="hero_text">
        Currently working as a <span class="spaned_text">Product Designer</span> at <span class="spaned_text">Access Bank.</span>
      </p>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.hero_ctn {
  height: 80vh;
  background-color: #000;
  display: flex;
  align-items: center;
}

.hero_inner {
  max-width: 1344px;
  width: 70%;
  margin: auto;
}

.hero_head {
  color: #fff;
  font-family: Power Grotesk;
  font-size: 76px;
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
