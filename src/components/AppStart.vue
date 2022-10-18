<template>
  <div class="start">
    <div class="container">
      <div class="left-block">
        <p class="topP">START WITH US</p>
        <h2>{{ h2 }}</h2>
        <p>
          We know the best solution for all of your business ideas and we can help you
          solve all business problems
        </p>
        <button @click="this.$emit('showModal')">{{ btnStart }}</button>
      </div>
      <div class="right-block">
        <div class="start-img">
          <div>
            <img style="z-index: 1" src="../assets/vectorStart.svg" />
            <img class="startImg" style="z-index: 2" src="../assets/startImg.png" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppStart",
  props: {
    btnStart: {},
  },
  data() {
    return {
      h2: "Start working faster today",
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
}
h2 {
  font-weight: 500;
  font-size: 48px;
  line-height: 122%;
  margin: 10px 0 10px 0;
}
.topP {
  margin-top: 50px;
}
p,
h2 {
  color: #ffffff;
  max-width: 350px;
  text-align: left;
}
p {
  line-height: 34px;
}
.start {
  min-height: 870px;
  background: linear-gradient(249.78deg, #35d3ff -0.64%, #a963fb 103.6%);
  display: flex;
  justify-content: center;
  color: #ffffff;
  border-top-left-radius: 250px 250px;
}
img {
  position: relative;
}
img:first-child {
  right: 170px;
  position: absolute;
}
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .left-block {
    position: relative;
    align-items: center;
  }
  p,
  h2 {
    text-align: center;
    max-width: 100%;
  }
}
.right-block,
.left-block {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.startImg {
  width: 100%;
  max-width: 593px;
}
</style>
