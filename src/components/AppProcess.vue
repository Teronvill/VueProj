<template>
  <div class="process">
    <img class="vector vector3_1" src="../assets/vector3_1.svg" />
    <img class="vector vector3_2" src="../assets/vector3_2.svg" />
    <img class="vector vector3_3" src="../assets/vector3_3.svg" />
    <img class="vector vector3_4" src="../assets/vector3_4.svg" />
    <div class="container">
      <p class="topP">HOW IT WORKS</p>
      <h2>{{ h2 }}</h2>
      <p>
        We know the best solution for all of your business ideas and we can help you solve
        all business problems
      </p>
      <div class="items">
        <div v-for="item in purposes" :key="item.id" class="item">
          <div class="left-item"><img :src="item.img" /></div>
          <div class="right-item">
            <div class="itemImg" :style="{ backgroundColor: item.color }">
              <img :src="item.src" />
            </div>
            <div class="title">
              <h3>{{ item.title }}</h3>
            </div>
            <div class="content">
              {{ item.text }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppProcess",
  props: {},
  data() {
    return {
      h2: "Our Process",
      purposes: [
        {
          title: "Business Audit",
          text:
            "An audit examines your business's financial records to verify they are accurate. This is done through a systematic review of your transactions.",
          src: require("../assets/item-icon3_1.svg"),
          img: require("../assets/item-img3_1.png"),
          color: "#DAE6FF",
        },

        {
          title: "Data tracking",
          text:
            "The hardware and software, which when used together allows you to know where something is at any point in time",
          src: require("../assets/item-icon3_2.svg"),
          img: require("../assets/item-img3_2.png"),
          color: "#E9E6FF",
        },

        {
          title: "Results",
          text:
            "An audit examines your business's financial records to verify they are accurate. This is done through a systematic review of your transactions.",
          src: require("../assets/item-icon3_3.svg"),
          img: require("../assets/item-img3_3.png"),
          color: "#CEEDFF",
        },
      ],
    };
  },
};
</script>

<style scoped>
h2 {
  color: #ffffff;
  line-height: 122%;
  margin-top: 10px;
}
.topP {
  margin-top: 50px;
}
p {
  color: #ffffff;
  position: relative;
}
.process {
  min-height: 1450px;
  background: linear-gradient(249.78deg, #35d3ff -0.64%, #a963fb 103.6%);
  display: flex;
  justify-content: center;
}
.items {
  z-index: 3;
}
.item {
  margin-top: 40px;
  display: flex;
  background: #ffffff;
  column-count: 2;
  width: 100%;
  max-width: 1200px;
  box-shadow: 0px 20px 50px rgba(59, 62, 67, 0.05);
  border-radius: 15px;
  text-align: left;
  line-height: 24px;
}
.itemImg {
  width: 50px;
  height: 50px;
  box-shadow: 0px 10px 20px rgba(197, 158, 145, 0.1);
  border-radius: 15px;
}
.itemImg img {
  height: 28px;
  width: 28px;
  margin: 11px;
}
.left-item {
  width: 50%;
  min-width: 400px;
  display: flex;
  justify-content: center;
}
.left-item img {
  max-width: 100%;
  padding-left: 10px;
  padding-top: 10px;
}
.right-item {
  width: 50%;
  padding: 75px 90px 60px 60px;
}
.vector3_1 {
  left: 0;
}
.vector3_2 {
  right: 0;
}
.vector3_3 {
  right: 0;
  top: 3200px;
}
.vector3_4 {
  left: 0;
  top: 3350px;
}
@media (max-width: 768px) {
  .item {
    padding-top: 50px;
    flex-wrap: wrap;
    justify-content: center;
    text-align: center;
  }
  .right-item * {
    display: flex;
    justify-content: center;
  }
  .itemImg {
    width: 100%;
  }
  .left-item {
    min-width: 100%;
  }
}
</style>
