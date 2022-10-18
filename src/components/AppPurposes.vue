<template>
  <div class="purposes">
    <img class="vector vector2_1" src="../assets/vector2_1.svg" />
    <img class="vector vector2_2" src="../assets/vector2_2.svg" />
    <div class="container">
      <p class="topP">FEATURES</p>
      <h2>{{ h2 }}</h2>
      <div class="items">
        <div v-for="item in purposes" :key="item.id" class="item"><div class="itemImg" :style={backgroundColor:item.color}><img 
          :src="item.src"></div>
        <div class="title"><h3>{{item.title}}</h3></div>
        <div class="content">
          {{item.text}}
        </div></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppPurposes',
  props: {
  },
  data(){
      return{
        h2:'We are here to help you with',
        purposes:[
          {title:'Grow your business',
          text:'The magic wand for success is in figuring out how to bring in the profits and ensure the capacity needed to sustain that growth for posterity.',
          src:require('../assets/item-icon1.svg'), 
          color:'#FFE7DB'},
          
          {title:'Drive more sales',
          text:'A potential customer, once lost, is hard to retain back. But keeping some critical factors in mind, we can, for sure, use these loyalty programs as customer retention tools.',
          src:require('../assets/item-icon2.svg'),
          color:'#E7F2EF'},

          {title:'Handle by Expert', 
          text:'We know how we candevelop deep, trust-based relationships with our clients, and work together more collaboratively',
          src:require('../assets/item-icon3.svg'),
          color:'#FAF3D8'},
          
          {title:'UX Research',
          text:'UX research is the systematic study of target users and their requirements, to add realistic contexts and insights to design processes.',
          src:require('../assets/item-icon4.svg'),
          color:'#C0F2EF'},
         
          {title:'Business Audit',
          text:"An audit examines your business's financial records to verify they are accurate. This is done through a systematic review of your transactions. ",
          src:require('../assets/item-icon5.svg'),
          color:'#EDE7F2'},
          
          {title:'Data tracking',
          text:'The hardware and software, which when used together allows you to know where something is at any point in time',
          src:require('../assets/item-icon6.svg'),
          color:'#D8F0FA'}
        ],
  
      }
  },
}
</script>
<style scoped>
.purposes {
  min-height: 880px;
  color:#595E64;
  font-size: 16px;
  text-align: left;
  display: flex;
  justify-content: center;
  padding-top: 90px;
}
.items{
  display: flex;
  flex-wrap: wrap;

}
@media (max-width: 768px) {
  .items{
    flex-direction: column;
    flex-wrap: nowrap;
  }
  .vector2_1 {
    height: 400px;
    width: 350px;
  }
  .vector2_2 {
    height: 400px;
    width: 400px;
  }
}
.item {
  z-index: 3;
  flex:25%;
  margin-right: 30px;
  margin-bottom: 25px;
  padding: 40px 22px 40px 30px;
  background-color: #FFFFFF;
  line-height: 24px;
  box-shadow: 0px 20px 50px rgba(59, 62, 67, 0.05);
  border-radius: 15px;
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
h2 {
  margin-top: 0;
  text-align: left;
  color: #3b3e43;
}
.vector2_1{
left: -100px;
top: 1675px;
}
.vector2_2{
  right: 0px;
}
</style>
