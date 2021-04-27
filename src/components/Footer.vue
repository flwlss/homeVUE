<template>
  <footer class="footer footer_bg">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="footer__logo">
            <img
              src="../assets/images/footer-logo.png"
              alt=""
              class="footer__img"
            />
          </div>
          <ul class="footer__socials">
            <li class="footer__social">
              <a href="#" target="blank"
                ><img
                  src="../assets/images/icons/f.png"
                  alt=""
                  class="footer__pic"
              /></a>
            </li>
            <li class="footer__social">
              <a href="#" target="blank"
                ><img
                  src="../assets/images/icons/p.png"
                  alt=""
                  class="footer__pic"
              /></a>
            </li>
            <li class="footer__social">
              <a href="#" target="blank"
                ><img
                  src="../assets/images/icons/insta.png"
                  alt=""
                  class="footer__pic"
              /></a>
            </li>
            <li class="footer__social">
              <a href="#" target="blank"
                ><img
                  src="../assets/images/icons/g+.png"
                  alt=""
                  class="footer__pic"
              /></a>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3 class="footer__title">Navigation</h3>
          <ul class="footer__list footer__list_capitalize">
            <li v-for="({ name, path }, i) in footerMenu" :key="i">
              <router-link :to="path" class="footer__link">{{
                name
              }}</router-link>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3 class="footer__title">For clients</h3>
          <ul class="footer__list footer__list_capitalize">
            <li v-for="({ name, path }, i) in footerMenuClient" :key="i">
              <router-link :to="path" class="footer__link">{{
                name
              }}</router-link>
            </li>
          </ul>
        </div>
        <div class="col">
          <h3 class="footer__title">Contact us</h3>
          <ul class="footer__list footer__list_capitalize">
            <li>
              <p>240 Central Park, London Or 10019</p>
            </li>
            <li>
              <p>Freephone: +1 800 559 6580</p>
              <p>Telephone: +1 959 603 6035</p>
              <p>FAX: +1 8</p>
            </li>
            <li>
              <a
                class="footer__link footer__link_red"
                href="mailto:info@realhome.com"
                target="blank"
                >info@realhome.com</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import { menuList, menuClient } from "../constants/menuLinks";

export default {
  data() {
    return {
      footerMenu: menuList,
      footerMenuClient: menuClient,
    };
  },
};
</script>
<style lang="">
</style>