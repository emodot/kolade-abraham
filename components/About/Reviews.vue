<template>
  <div class="review_ctn">
    <div class="review_inner">
      <div class="lhs">
        <h1 class="review_header">Reviews.</h1>
        <p class="review_subheader">What people say about Kola.</p>
        <div class="review_box">
          <p class="review_text">"I highly recommend Kolade as a multidisciplinary designer. His ability to seamlessly integrate multiple design disciplines and deliver exceptional results is truly impressive. He is a true master of his craft and a pleasure to work with. I have no doubt that he will continue to excel in his career."</p>
          <div class="review_details">
            <p class="author">Nathaniel Ike,</p>
            <p class="work">Forbes Africa 30 U’ 30</p>
            <img class="review_rating" src="~assets/icons/5-star-rating.svg" alt="">
          </div>
        </div>
        <div class="review_box">
          <p class="review_text">"When it comes to creating great designs, I have known Kolade Abraham for some years now as a competent designer with the ability to create great designs seamlessly. When It comes to delivering exceptional creative results, I highly recommend him and I have no doubt he will deliver.."</p>
          <div class="review_details">
            <p class="author">‘dimeji Oyeniran,</p>
            <p class="work">Brand Consultant</p>
            <img class="review_rating" src="~assets/icons/5-star-rating.svg" alt="">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.review_ctn {
  height: 100vh;
  background-image: url('assets/images/review-bg.webp');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.review_inner {
  max-width: 1344px;
  width: 70%;
  margin: auto;
  height: 100%;
  display: flex;
  align-items: center;
}

.lhs {
  width: 45%;
}

.review_header {
  color: #9EA3B0;
  font-family: Power Grotesk;
  font-size: 72px;
  font-style: normal;
  font-weight: 500;
}

.review_subheader {
  font-size: 18px;
}

.review_box {
  margin-top: 40px;
}

.review_text {
  color: #ffffff;
  font-family: var(--nunito);
  font-style: italic;
  font-size: 16px;
  line-height: 26px;
}

.review_details {
  display: flex;
  align-items: center;
  margin-top: 20px;
}

.author {
  color: #ffffff;
  font-family: var(--nunito);
  font-size: 16px;
  font-weight: 700;
  margin-right: 10px;
}

.work {
  font-size: 16px;
  font-family: var(--nunito);
  font-weight: 700;
  margin-right: 20px;
}

.review_rating {
  width: 20%;
  margin-bottom: 5px;
}
</style>