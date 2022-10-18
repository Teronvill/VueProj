<template>
  <AppHeader :btnStart="btnStart" :menu="menu" :logo="logo" :adress="hrefs[0]" @scroll="scroll" @showModal="showModal"/>
  <AppPurposes/>
  <AppProcess/>
  <AppPartners/>
  <AppStart :btnStart="btnStart" @showModal="showModal"/>
  <AppFooter :menu="menu" :logo="logo" :hrefs="hrefs" @scroll="scroll"/>
  <AppModalStart :flag="flagModal" @closeModal="closeModal"/>
</template>

<script>

import AppHeader from "./components/AppHeader.vue"
import AppPurposes from "./components/AppPurposes.vue"
import AppProcess from "./components/AppProcess.vue"
import AppPartners from "./components/AppPartners.vue"
import AppStart from "./components/AppStart.vue"
import AppFooter from "./components/AppFooter.vue"
import AppModalStart from "./components/AppModalStart.vue"
export default {
  name: 'App',
  data() {return{
    hrefs:["http://mysite/",
            "https://facebook.com/",
            "https://instagram.com",
            "https://twitter.com",
            "https://privacy.com/",
            "https://termofservice.com"
            ],
    btnStart:"Get Started",
    flagModal:false,
    menu: [
        "Home",
        "Your benefits",
        "Our process",
        "Testimonials",
        "Start a project",
      ],
      logo:require("./assets/logo.png"),

  }},
  components: {
    AppHeader,
    AppPurposes,
    AppProcess,
    AppPartners,
    AppStart,
    AppFooter,
    AppModalStart
},
methods: {
  scroll:(num)=>{
    let scrollTarget=document.querySelector("#app").childNodes[num+1];
    scrollTarget.scrollIntoView({behavior: "smooth"});
  },
  showModal:function(){
      this.flagModal=true;
      console.log('asd');
      
  },
  closeModal:function(){
        this.flagModal=false;
      }
},
}
</script>

<style>
body {
  margin: 0;
}
#app {
  background-color:#F9F8FF;
  @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap');
  font-family: 'DM Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #595E64;
}
.container{
  display: flex;
  flex-direction: column;
  max-width: 1280px;
  width: 100%;
  justify-content: center;
  
}
.vector{
  position: absolute;
}
.topP{
  color:#00A077;
  font-weight: 700;
  font-size: 12px;
  opacity: 0.5;
  letter-spacing: 0.15em;
  }
  h2{
    position: relative;
    font-size: 48px;
    font-weight: 500;
  }
  h3{
    color:#3B3E43;
    font-size:22px;
    font-weight: 700;
    margin: 20px 0 15px 0;
  }
  button {
    position: relative;
    height: 62px;
    width: 194px;
    background-color: #ffffff;
    border-radius: 60px;
    border: none;
    font-weight: 700;
    font-size: 16px;
    color: #57b3fe;
  }
  @media (max-width: 768px) {
    button{
      height: 37px;
    width: 110px;
    }
  }
  li{
    cursor: pointer;
  }
</style>
