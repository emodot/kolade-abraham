<template>
  <div class="hero_ctn">
    <div class="hero_inner">
      <h1 class="hero_head">{{ greetings[currentGreetingIndex] }},</h1>
      <p class="hero_text">
        I am ‘Kola, I like to make digital experiences
        <span class="spaned_text wavy">easier and simpler</span> for people.
      </p>
      <p class="hero_text">
        Currently working as a
        <span class="spaned_text">Product Designer</span> at
        <span class="spaned_text">Access Bank.</span>
      </p>
    </div>
  </div>
</template>

<script setup>
const { $gsap } = useNuxtApp();
const greetings = ref(['Hello', 'Bonjour', 'Namaste']);
const currentGreetingIndex = ref(0);

function updateGreeting() {
  currentGreetingIndex.value = (currentGreetingIndex.value + 1) % greetings.value.length;
}

setInterval(updateGreeting, 3000);

onMounted(() => {
  $gsap.from(".hero_inner", { y: 200, duration: 1 });
});

// const animateText = () => {

// };
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
  width: 70%;
  margin: auto;
}

.hero_head {
  color: #fff;
  font-family: Power Grotesk;
  font-size: 76px;
  font-style: normal;
  font-weight: 500;
  transition: opacity 0.5s, transform 0.5s;
}

.hero_head.out {
  opacity: 0;
  transform: translateX(50px);
}

.hero_head.in {
  opacity: 1;
  transform: translateX(0);
}

.hero_text {
  color: var(--text-color);
  font-size: 20px;
  margin-top: 15px;
  line-height: 26px;
}

.spaned_text {
  color: #b8b8b8;
  font-size: inherit;
}

.wavy {
  text-decoration: underline;
  text-decoration-color: var(--text-color);
  text-decoration-style: wavy;
}

@media only screen and (max-width: 1200px) {
  .hero_ctn {
    height: 80vh;
  }

  .hero_inner {
    width: 85%;
  }

  .hero_head {
    font-size: 56px;
  }

  .hero_text {
    font-size: 16px;
  }
}
</style>
