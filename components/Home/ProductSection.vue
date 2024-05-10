<template>
  <div class="product_ctn">
    <div class="product_inner">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="product_section"
        :class="index % 2 !== 0 ? 'reversed_section' : ''"
      >
        <div class="section_lhs">
          <img :src="`${project.image}`" alt="" />
        </div>
        <div class="section_rhs">
          <div class="rhs_inner">
            <h1 class="product_head">{{ project.name }}</h1>
            <p class="product_text">
              {{ project.description }}
            </p>
            <a :href="project.link" :target="`${project.link === '#' ? '_self' : '_blank'}`"><button class="global_btn">View Details</button></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const projects = ref([
  {
    name: "Vaccess App",
    description:
      "Vaccess provides a seamless mobile app and website, streamlining Lagos vaccination center searches with real-time data, intuitive interfaces, and appointment booking.",
    image: "/vaccess.png",
    link: "https://abrahamkola.notion.site/Vaccess-Responsive-Web-Mobile-App-1051448714be48a0b3534adc42d6596d",
  },
  {
    name: "Tra-it AR App",
    description:
      "Tra-it AR offers virtual 'try-out' of ecommerce products, from furniture to clothes, in true-to-scale AR view, before purchase.",
    image: "/ar-app.png",
    link: "https://abrahamkola.notion.site/Tra-it-f3752f7264d1488ba7e3c2885dedb187",
  },
  {
    name: "OpsPad",
    description:
      "OpsPad streamlines DevOps workflow with a minimalist notepad design for monitoring and analyzing infrastructure performance.",
    image: "/opspad.png",
    link: "https://www.behance.net/gallery/170294819/Opspad-Server-Management-Platform-UXUI-Case-Study",
  },
  {
    name: "Craigslist",
    description:
      "Craigslist's redesign mimics a newspaper's classifieds, facilitating local business ads, individual sales, and event postings, allowing user responses.",
    image: "/craigslist.png",
    link: "https://www.behance.net/gallery/159255543/Craigslist-Website-Redesign",
  },
  {
    name: "FELA",
    description:
      "Most farmers cannot afford to buy tractors outright or secure traditional loans due to a lack of collateral. FELA app connects farmers with equipment providers for leasing solutions.",
    image: "/fela.png",
    link: "https://www.behance.net/gallery/159102707/Farming-Equipment-Leasing-App",
  },
  {
    name: "Kairos Atelier",
    description:
      "Kairos Atelier uses design to address human issues with empathy and innovative solutions, operating as a multidisciplinary studio in architecture, art, and tech.",
    image: "/kairos.png",
    link: "https://kairos-atelier.webflow.io/",
  },
]);
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

.product_head {
  color: #232323;
  font-family: Power Grotesk;
  font-size: 44px;
  font-weight: 500;
}

.product_text {
  font-size: 16px;
  margin-top: 15px;
  margin-bottom: 30px;
  line-height: 28px;
}

@media only screen and (max-width: 1200px) {
  .product_inner {
    width: 85%;
  }
}

@media only screen and (max-width: 500px) {
  .product_ctn {
    padding: 5rem 0;
  }
  .product_section {
    flex-direction: column;
    margin-bottom: 5rem;
  }

  .section_lhs {
    flex-basis: 100%;
    margin-bottom: 40px;
  }

  .rhs_inner {
    width: 100%;
  }

  .product_head {
    font-size: 35px;
  }
}
</style>
