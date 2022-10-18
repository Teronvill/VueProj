<template>
  <div class="partners">
    <div class="container">
      <p class="topP">BRANDS</p>
      <h2>{{ h2 }}</h2>
      <div class="brands">
        <div class="brands-row1">
          <img v-for="img in brandsR1" :key="img.id" :src="img" alt="" />
        </div>
        <div class="brands-row2">
          <img v-for="img in brandsR2" :key="img.id" :src="img" alt="" />
        </div>
      </div>
      <p>You're going to be in good company. We work with world's leading brands.</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "AppPartners",
  data() {
    return {
      h2: "We work with thousands of the world’s leading brands",
      brandsR1: [
        require("../assets/brand1.png"),
        require("../assets/brand2.png"),
        require("../assets/brand3.png"),
        require("../assets/brand4.png"),
        require("../assets/brand5.png"),
      ],
      brandsR2: [
        require("../assets/brand6.png"),
        require("../assets/brand7.png"),
        require("../assets/brand8.png"),
        require("../assets/brand9.png"),
        require("../assets/brand10.png"),
      ],
    };
  },
};
</script>

<style scoped>
h2 {
  color: #3b3e43;
  font-weight: 500;
  font-size: 48px;
  line-height: 122%;
  margin-top: 10px;
}
.partners {
  position: relative;
  z-index: 3;
  background: #f9f8ff;
  display: flex;
  justify-content: center;
}
@media (max-width: 768px) {
  .brands-row1,
  .brands-row2 {
    flex-wrap: wrap;
  }
}
.brands-row1,
.brands-row2 {
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
  margin-bottom: 40px;
}
img {
  width: 155px;
  height: 60px;
}
</style>
