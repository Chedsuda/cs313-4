<template>
 <div id="app">
    <HelloWorld msg="HOW YOU LIKE THAT" />
    <hr>
    <div class="row">
      <div class="col-6">
      <img src="https://www.thairath.co.th/media/dFQROr7oWzulq5FZUIVSBeUQTlzGSEwA6WlhjytHWh2L2Hh4PNjIMk9lk4oT5D6FAC4.jpg" width="300" height="200" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
      <img src="https://pbs.twimg.com/profile_images/1289209780670586881/iR37XzeU_400x400.jpg" width="200" height="200" />

        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <CsButton @cc="sum" />
      </div>
      <div class="col-6">
        <CsButton @cc="sum1" />
      </div>
    </div>
    
  </div>
</template>
<script>
import HelloWorld from "./components/HelloWorld.vue";
import CsButton from "./components/CsButton";
export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
    
  },
  data : function(){
    return {
    total1: 0,
    total2: 0,
   
   } 
  },
  methods: {
  sum(counterValue){
    this.total1 = counterValue
  },
  
  sum1(counterValue){
    this.total2 = counterValue
 
  
},
},

};

</script>

<style>
body {
      background-image: url(https://downloadwap.com/thumbs2/wallpapers/p2ls/new/37/btfDXCuT.jpg);
      background-size: 90%;
    }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #d8e663;
  margin-top: 60px;
}
</style>