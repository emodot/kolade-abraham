<template>
  <div class="about_ctn">
    <div class="about_inner">
      <div class="about_section">
        <div class="section_text_side">
          <div class="text_side_inner">
            <h1 class="about_head">Who am I?</h1>
            <p class="about_text">
              My name is <span class="bold_text">Kolade</span> and I’m a <span class="bold_text">Product Designer based in Lagos, NG.</span> I
              have a Masters in Architecture, and a background in Graphics
              design.
            </p>
          </div>
        </div>
        <div class="section_image_side">
          <img src="assets/images/1.webp" alt="" />
        </div>
      </div>
      <div class="about_section reversed_section">
        <div class="section_text_side">
          <div class="text_side_inner">
            <h1 class="about_head">What do I do?</h1>
            <p class="about_text">
              <span class="bold_text">As a technology geek and a person who loves to attend UX conferences. I also bring with me a diverse culture that influences my design.</span> My background in Architecture also helps me look at design from an ergonomics point of view in addition to advocating for user’s needs and desires.
            </p>
            <p class="about_text">
              <span class="bold_text">Currently, I'm designing experiences for Access Bank.</span>
            </p>
          </div>
        </div>
        <div class="section_image_side">
          <img src="assets/images/2.webp" alt="" />
        </div>
      </div>
      <div class="about_section">
        <div class="section_text_side">
          <div class="text_side_inner">
            <h1 class="about_head">What am I passionate about?</h1>
            <p class="about_text">
              <span class="bold_text">I have a healthy obsession with how people interact with technology and connect people to ideas in a way that generates excitement.</span> I am curious and I like diving deep into emerging tech and latest trends to know more new spaces
            </p>
          </div>
        </div>
        <div class="section_image_side">
          <img src="assets/images/3.webp" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.about_ctn {
  background-color: #fff;
  padding: 10rem 0;
}

.about_inner {
  max-width: 1344px;
  width: 55%;
  margin: auto;
}

.about_section {
  /* width: 90%; */
  display: flex;
  justify-content: center;
  margin-bottom: 14rem;
}

.reversed_section {
  flex-direction: row-reverse;
  justify-content: left;
}

.reversed_section > .section_image_side {
  margin-right: 15rem;
  margin-left: 0;
}

.section_image_side {
  flex-basis: 30%;
  margin-top: -50px;
  margin-left: 15rem;
}

.section_image_side img {
  width: 100%;
}

.section_text_side {
  flex-basis: 65%;
}

.text_side_inner {
  width: 100%;
}

.about_head {
  color: #232323;
  font-family: Power Grotesk;
  font-size: 50px;
  font-weight: 500;
}

.about_text {
  font-size: 16px;
  margin-top: 15px;
  margin-bottom: 30px;
  line-height: 28px;
}

.bold_text {
  font-weight: 700;
  font-size: 16px;
  margin-top: 15px;
  margin-bottom: 30px;
  line-height: 28px;
  color: #000000;
}
</style>
