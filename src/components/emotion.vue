<template>
  <div id="example-1">    
    <p v-bind:style="{fontSize: fsize + 'px' }"> Score : {{ count }} </p>    
    <button @click="LikeFunction()">
      <!-- <i class="fas fa-thumbs-up" style='color:white'></i> -->
      <img src="./images/like.png">
    </button>
    <button @click="LoveFunction()">
      <!-- <i class="fas fa-heart"></i> -->
      <img src="./images/love.png">
      </button>
    <button @click="HahaFunction()">
      <!-- <i class="fas fa-laugh-squint" style='color:white'></i> -->
      <img src="./images/haha.png">
    </button>
    <button @click="WowFunction()">
      <!-- <i class="fas fa-surprise"></i> -->
      <img src="./images/wow.png">
      </button>
    <button @click="SadFunction()">
      <!-- <i class="far fa-frown-open"></i> -->
      <img src="./images/sad.png">
      </button>
    <button @click="AngryFunction()">
      <!-- <i class="fas fa-angry"></i> -->
      <img src="./images/angry.png">
      </button>
    
      

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