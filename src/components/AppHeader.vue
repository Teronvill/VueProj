<template>
  <div class="header">
    <img class="vector vector1" src="../assets/vector1.svg" />
    <img class="vector vector2" src="../assets/vector2.svg" />
    <img class="vector vector3" src="../assets/vector3.png" />
    <img class="vector vector4" src="../assets/vector4.svg" />
    <div class="headerTop">
      <div class="icon">
        <a :href="adress">
          <img alt="logo" :src="logo" />
        </a>
      </div>
      <ul>
        <li v-for="(a, index) in menu" :key="index">
          <div @click="this.$emit('scroll', index)">{{ a }}</div>
        </li>
      </ul>
      <button @click="this.$emit('showModal')">{{ btnStart }}</button>
    </div>
    <div class="headerBottom">
      <div class="title">
        <h1>{{ Title }}</h1>
        <p>We are Creative and Professional Digital Agency</p>
      </div>
      <button @click="this.$emit('showModal')">{{ btnStart }}</button>
      <div class="content">
        <img alt="logo" src="../assets/header-img.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    btnStart: String,
    menu: [],
    logo: String,
    adress: String,
  },
  data() {
    return {
      Title: "A Digital Product Design Agency",
    };
  },
};
</script>

<style scoped>
.header {
  border-bottom-right-radius: 350px 350px;
  background: linear-gradient(249.78deg, #35d3ff -0.64%, #a963fb 103.6%);
  color: #ffffff;
}
.content img {
  position: relative;
  width: 100%;
  max-width: 1280px;
}
.vector1 {
  right: 0;
}
.vector2 {
  top: 700px;
  left: 200px;
}
.vector3 {
  z-index: 1;
  left: 0;
  top: 0;
  height: 352px;
  width: 352px;
}
.vector4 {
  right: 2px;
  top: 440px;
}
.headerTop {
  display: flex;
  justify-content: space-between;
  margin: 0 70px 0 60px;
  padding-top: 45px;
  height: 61px;
}
.headerBottom {
  position: relative;
  z-index: 2;
}
h1 {
  height: 88px;
  margin: 105px 0px 8px 0px;
  font-size: 64px;
  color: #ffffff;
}
h3 {
  font-weight: 400;
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
.title {
  margin-bottom: 41px;
}
.title p {
  color: #ffffff;
  font-size: 20px;
  font-weight: 400;
  margin: 8px;
}
.icon img {
  max-width: 240px;
  position: relative;
  z-index: 2;
}
@media (max-width: 1024px) {
  h1 {
    font-size: 50px;
  }
}
@media (max-width: 768px) {
  .brands-row1,
  .brands-row2 {
    flex-wrap: wrap;
  }
  .vector {
    width: 100px;
    height: 100px;
  }
  .vector2 {
    display: none;
  }
  .icon img {
    max-width: 120px;
  }
  h1 {
    font-size: 44px;
  }
  ul {
    display: none;
  }
}
</style>
