<template>
    <div v-if="flag" class="modal">
      <div class="modal__Back"></div>
      <div class="container">
        <div class="modal__window">
          <div class="close">
            <button @click="this.$emit('closeModal')" class="modal__close">Close</button>  
          </div>
            <h3>Сontact us</h3>
            <input type="text" name="name" placeholder="Enter name">
            <input type="text" name="Phone" placeholder="Enter phone">
            <input type="text" name="E-mail" placeholder="Enter e-mail">
            <button class="modal__submit">Submit</button>  
        </div>
      </div>
    </div>
  </template>
  <script>
  export default {
    name: "AppModalStart",
    props: {
      logo: String,
      flag:Boolean
    },
    data() {
      return {
      };
    },
  };
  </script>
  <style scoped>
 .modal {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    overflow: hidden;
    overflow-y: auto;
    -webkit-overflow-scrolling: touch;
    display: flex;
    flex-flow: column nowrap;
    justify-content: center;
    align-items: center;
    z-index: 99;
    padding:30px 0;
}
.container{
  align-items: center;
}
.modal__window {
  z-index: 3;
    background: #fff;
    display: flex;
    flex-direction: column;
    width: 650px;
    max-width: 100%;
    border: solid 7px #FFFFFF;
    border-radius: 25px;
    background: linear-gradient(249.78deg, #35d3ff -0.64%, #a963fb 103.6%);
    align-items: center;
}
.modal__Back{
  position:fixed;
  z-index: 2;
    top:0;
    left:0;
    width:100vw;
    height:100vh;
    background-color:rgba(0,0,0,0.3);
}
h3{ 
  margin-top: 10px;
  font-size: 42px;
  color:#FFFFFF;
  font-weight: 500;
}
input {
  height: 35px;
  margin: 15px 35px 0 35px;
  border:none;
  text-align: center;
  border-radius: 25px;
  width: 70%;
  font-size: 22px;

}
input:focus{
  outline: #FFFFFF solid 1px;
}
.modal__close{
  width: 75px;
  height: 40px;
}
button{
  margin:15px;
  font-size:16px;
  transition: 0.5s;
}

.close {
  display: flex;
  width: 100%;
  justify-content: end;
}
.modal__submit{
  margin-top: 30px;
}

  </style>
  