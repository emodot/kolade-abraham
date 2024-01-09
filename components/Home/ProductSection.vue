<template>
  <div class="product_ctn">
    <div class="product_inner">
      <div v-for="(project, index) in projects" :key="index" class="product_section" :class="index % 2 !== 0 ? 'reversed_section' : ''">
        <div class="section_lhs">
          <img :src="`_nuxt/${project.image}`" alt="" />
        </div>
        <div class="section_rhs">
          <div class="rhs_inner">
            <h1 class="product_head">{{ project.name }}</h1>
            <p class="product_text">
              {{ project.description }}
            </p>
            <button class="global_btn">
              View Details
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const projects = ref([
  {
    name: 'Vaccess App',
    description: 'Vaccess provides a seamless mobile app and website, streamlining Lagos vaccination center searches with real-time data, intuitive interfaces, and appointment booking.',
    image: 'assets/images/vaccess.png',
    link: '',
  },
  {
    name: 'Tra-it AR App',
    description: 'Tra-it AR offers virtual \'try-out\' of ecommerce products, from furniture to clothes, in true-to-scale AR view, before purchase.',
    image: 'assets/images/ar-app.png',
    link: '',
  },
  {
    name: 'OpsPad',
    description: 'OpsPad streamlines DevOps workflow with a minimalist notepad design for monitoring and analyzing infrastructure performance.',
    image: 'assets/images/opspad.png',
    link: '',
  },
  {
    name: 'Craigslist',
    description: 'Craigslist\'s redesign mimics a newspaper\'s classifieds, facilitating local business ads, individual sales, and event postings, allowing user responses.',
    image: 'assets/images/craigslist.png',
    link: '',
  },
  {
    name: 'FELA',
    description: 'Most farmers cannot afford to buy tractors outright or secure traditional loans due to a lack of collateral. FELA app connects farmers with equipment providers for leasing solutions.',
    image: 'assets/images/fela.png',
    link: '',
  },
  {
    name: 'Kairos Atelier',
    description: 'Kairos Atelier uses design to address human issues with empathy and innovative solutions, operating as a multidisciplinary studio in architecture, art, and tech.',
    image: 'assets/images/kairos.png',
    link: '',
  },
])

</script>

<style scoped>
.product_ctn {
  background-color: #fff;
  padding: 10rem 0;
}

.product_inner {
  max-width: 1344px;
  width: 70%;
  margin: auto;
}

.product_section {
  /* width: 90%; */
  display: flex;
  justify-content: space-between;
  margin-bottom: 14rem;
}

.reversed_section {
  flex-direction: row-reverse;
  justify-content: left;
}

.section_lhs {
  flex-basis: 45%;
}

.section_lhs img {
  width: 100%;
  border-radius: 10px;
}


.section_rhs {
  flex-basis: 45%;
}

.rhs_inner {
  width: 75%;
}

.product_text {
font-size: 16px;
margin-top: 15px;
margin-bottom: 30px;
line-height: 28px;
}
</style>
