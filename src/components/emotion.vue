<template>
  <div id="example-1">    
    <p v-bind:style="{fontSize: fsize + 'px' }"> Score : {{ count }} </p> 
    <div class="row mb-5 ">
    <div class="col-md-2" >   
    <button @click="LikeFunction()">
      <img src="./images/like.png">
    </button></div>
    <div class="col-md-2">
    <button @click="LoveFunction()">
      <img src="./images/love.png">
      </button></div>
    <div class="col-md-2">  
    <button @click="HahaFunction()">
      <img src="./images/haha.png">
    </button></div>
    <div class="col-md-2">
    <button @click="WowFunction()">
      <img src="./images/wow.png">
      </button></div>
    <div class="col-md-2">  
    <button @click="SadFunction()">
      <img src="./images/sad.png">
      </button></div>
    <div class="col-md-2">  
    <button @click="AngryFunction()">
      <img src="./images/angry.png">
      </button></div>
    </div>
    
      

  </div>
</template>

<script>
export default {
  data: function () {
    return {
      count: 0,
    }
  },
  methods:{
    LikeFunction: function(){
      this.count += 1
      this.$emit('cc',this.count)
    },
    LoveFunction: function(){
      this.count += 10
      this.$emit("cc", this.count);
    },
    HahaFunction: function(){
      this.count += 5
      this.$emit("cc", this.count);
    },
    WowFunction: function(){
      this.count += 20
      this.$emit("cc", this.count);
    },
    SadFunction: function(){
      this.count -= 5
      this.$emit("cc", this.count);
    },
    AngryFunction: function(){
      this.count -= 50
      this.$emit("cc", this.count);
    },
    ResetFunction: function () {
      this.count = 0;
      this.$emit("cc", this.count);
    },
    sum(counterValue){
      this.total += counterValue
    },
  },
  props: {
    label: String
  },
};
</script>

<style>
</style>