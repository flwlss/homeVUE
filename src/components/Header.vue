<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <a class="navbar-brand logo" href="/"
        ><img src="../assets/images/logo.png" alt="logo"
      /></a>
      <div
        class="collapse navbar-collapse collapse-fontsize"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li
            class="nav-item menu-link"
            v-for="(menu, index) in headerList"
            :key="index"
          >
            <router-link
              class="nav-link active"
              aria-current="page"
              :to="menu.path"
              >{{ menu.name }}</router-link
            >
          </li>
        </ul>
        <div>
          <div class="icons">
            <a href="#" target="blank"><img src="../assets/images/icons/f.png" alt="" /></a>
            <a href="#" target="blank"><img src="../assets/images/icons/g+.png" alt="" /></a>
            <a href="#" target="blank"
              ><img src="../assets/images/icons/insta.png" alt=""
            /></a>
            <a href="#" target="blank"><img src="../assets/images/icons/p.png" alt="" /></a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import {menuList} from '../constants/menuLinks'
export default {
  name: "Header",
  props: {
    msg: String,
  },
  data() {
    return {
      headerList: menuList,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "../assets/layouts/index.scss";
.nav-bar {
  height: 90px;
}
.navbar-nav {
  height: 90px;
}
.logo {
  padding-right: 180px;
}
.collapse-fontsize {
  font-size: 18px;
}
.menu-link {
  padding: 25px 30px;
  &:hover {
    background-color: $greyLight;
  }
}
.icons {
  a {
    width: 30px;
    height: 30px;
    border: 1px solid $greyLight;
    text-align: center;
    border-radius: 50%;
    margin-right: 10px;
    display: inline-block;
  }
}
</style>
