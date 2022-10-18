<template>
  <div class="footer">
    <div class="container">
      <div class="footer-top">
        <a :href="hrefs[0]"> <img alt="logo" :src="logo" /></a>
        <ul>
          <li v-for="(a, index) in menu" :key="index">
            <span @click="this.$emit('scroll', index)">{{ a }}</span>
          </li>
        </ul>
        <div class="social">
          <a v-for="(svg, index) in socialImg" :key="index" :href="hrefs[index + 1]"
            ><img :src="svg" alt=""
          /></a>
        </div>
      </div>
      <hr />
      <div class="footer-bottom">
        <div><span>© 2021 Company</span></div>
        <div>
          <span><a :href="hrefs[4]">Privacy policy</a></span>
          <span><a :href="hrefs[5]">Term of service</a></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    menu: [],
    logo: String,
    hrefs: [],
  },
  data() {
    return {
      socialImg: [
        require("../assets/social1.svg"),
        require("../assets/social2.svg"),
        require("../assets/social3.svg"),
      ],
    };
  },
};
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  background-color: #0d0d0d;
  color: #ffffff;
  height: 241px;
}

img {
  width: 176px;
  height: 41px;
}
.social img {
  height: 20px;
  width: 20px;
  padding-left: 20px;
}
.footer-top {
  padding-top: 90px;
  font-weight: 500;
}
.footer-bottom {
  padding-top: 20px;
}
.footer-bottom span {
  font-weight: 400;
  font-size: 15px;
  padding-left: 12px;
}
.footer-top,
.footer-bottom {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
  font-weight: 700;
  font-size: 16px;
}
a {
  text-decoration: none;
  color: #ffffff;
}
hr {
  width: 100%;
  border: 1px solid #ffffff;
}
.social {
  display: flex;
  align-items: center;
}
@media (max-width: 768px) {
  ul {
    display: none;
  }
}
</style>
