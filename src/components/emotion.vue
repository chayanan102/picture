<template>
  <div id="example-1">
    <!--<button @click="upFunction()" class="btn btn-info">{{label}}</button>-->
    <p v-bind:style="{fontSize: fsize + 'px' }"> Score : {{ counter }} </p>
    <div class="row-md-10 "> 
    <button @click="LikeFunction()" class="btn btn-info">
      <i class="fas fa-thumbs-up" style='color:white'></i>
      <img src="./images/like.png" class="img-fluid" />
    </button>
    <button @click="LoveFunction()" class="btn btn-danger">
      <i class="fas fa-heart"></i>
      </button>
    <button @click="HahaFunction()" class="btn btn-warning">
      <i class="fas fa-laugh-squint" style='color:white'></i>
    </button>
    <button @click="WowFunction()" class="btn btn-success">
      <i class="fas fa-surprise"></i>
      </button>
    <button @click="SadFunction()" class="btn btn-info">
      <i class="far fa-frown-open"></i>
      </button>
    <button @click="AngryFunction()" class="btn btn-danger">
      <i class="fas fa-angry"></i>
      </button>
    </div>
      

  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
    }
  },
  methods:{
    LikeFunction: function(){
      this.counter += 1
      this.$emit('cc',this.counter)
    },
    LoveFunction: function(){
      this.counter += 10
      this.$emit("cc", this.counter);
    },
    HahaFunction: function(){
      this.counter += 5
      this.$emit("cc", this.counter);
    },
    WowFunction: function(){
      this.counter += 20
      this.$emit("cc", this.counter);
    },
    SadFunction: function(){
      this.counter -= 5
      this.$emit("cc", this.counter);
    },
    AngryFunction: function(){
      this.counter -= 50
      this.$emit("cc", this.counter);
    },
    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
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