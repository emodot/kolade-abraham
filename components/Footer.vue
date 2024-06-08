<template>
  <div class="footer_ctn">
    <div class="footer_inner">
      <div class="footer_top">
        <div class="footer_lhs">
          <p class="footer_head">GET IN TOUCH</p>
          <p class="email">Contact@abrahamkolade.com</p>
          <p class="location">Ontario, CA</p>
        </div>
        <div class="footer_rhs">
          <p class="footer_head">LET'S CONNECT</p>
          <div class="rhs_inner">
            <div class="lhs_links">
              <a
                class="links"
                href="https://www.linkedin.com/in/kolade-m-abraham/"
                target="_blank"
                >LinkedIn</a
              >
              <a
                class="links"
                href="https://twitter.com/Kola_Abr"
                target="_blank"
                >Twitter</a
              >
              <a
                class="links"
                href="https://abrahamkola.notion.site/b6a396aafc494f519b70d6ce1fada8ed#52097237c64945a2b72230d1b4980002"
                target="_blank"
                >Resume</a
              >
            </div>
            <div class="rhs_links">
              <a
                class="links"
                href="https://dribbble.com/kola_abr"
                target="_blank"
                >Dribbble</a
              >
              <a
                class="links"
                href="https://www.behance.net/kola_abr"
                target="_blank"
                >Behance</a
              >
            </div>
          </div>
        </div>
      </div>
      <div class="footer_bottom">
        <div class="bottom_lhs">
          <p class="made_with">Made with ♥ & ♫ | Kolade Abraham</p>
        </div>
        <div class="bottom_rhs">
          <p class="copyright">Copyrights © 2024</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
* {
  color: #575757;
}
.footer_ctn {
  background-color: #000;
  bottom: 0;
  width: 100%;
  padding: 5rem 0;
}

.footer_inner {
  max-width: 1344px;
  width: 70%;
  margin: auto;
}

.footer_top {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10rem;
}

.footer_bottom {
  display: flex;
  justify-content: space-between;
}

/* .bottom_lhs {
  flex-basis: 50%;
} */

.bottom_rhs {
  flex-basis: 40%;
}

.footer_head {
  color: #fff;
  font-size: 11px;
  margin-bottom: 30px;
}

.footer_rhs {
  flex-basis: 40%;
}

.email {
  color: #575757;
  font-size: 28px;
}

.location {
  color: #575757;
  font-size: 15px;
  margin-top: 5px;
}

.rhs_inner {
  display: flex;
  width: 50%;
  justify-content: space-between;
}

.lhs_links,
.rhs_links {
  display: flex;
  flex-direction: column;
}

a {
  text-decoration: underline;
}

.links {
  margin-bottom: 20px;
}

@media only screen and (max-width: 1200px) {
  .footer_inner {
    width: 85%;
  }
}

@media only screen and (max-width: 900px) {
  .footer_rhs {
    flex-basis: 30%;
    margin-top: 40px;
  }

  .rhs_inner {
    width: 70%;
    flex-direction: column;
  }

  .footer_top {
    flex-direction: column;
    margin-bottom: 4rem;
  }

  .email {
    font-size: 20px;
  }

  .footer_bottom {
    flex-direction: column;
  }

  .bottom_rhs {
    margin-top: 30px;
  }
}
</style>
