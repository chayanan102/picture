<template>
  <div id="app">
    <div class="container">      
      <div id="myCarousel" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
          <li data-target="#myCarousel" data-slide-to="0" class></li>
          <li data-target="#myCarousel" data-slide-to="1" class="active"></li>
          <li data-target="#myCarousel" data-slide-to="2" class></li>
        </ol>
        <div class="carousel-inner">
          <div class="carousel-item">
            <img :src="img[0].src" class="img-fluid" />
          </div>
          <div class="carousel-item active">
            <img :src="img[1].src" class="img-fluid" />
          </div>
          <div class="carousel-item">
            <img :src="img[2].src" class="img-fluid" />
          </div>
          <a class="carousel-control-prev" href="#myCarousel" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
          </a>
          <a class="carousel-control-next" href="#myCarousel" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
          </a>
        </div>
      </div>
    </div>
    <div class="container">
      <hr class="featurette-divider" />
      <div class="row featurette alert alert-success" style="opacity: 0.9; ">
        <div class="row align-items-center">
          <div class="col-6">
            <!-- 2.รับค่าจาก emit @cc แล้วส่งไปทำงานใน function "sum"-->
            <emotion label @cc="sum" />
          </div>
          <div class="col-6">
            <img :src="img[0].src" class="img-fluid" />
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <hr class="featurette-divider" />
      <div class="row featurette alert alert-success" style="opacity: 0.9; ">
        <div class="row align-items-center">
          <div class="col-6">
            <img :src="img[1].src" class="img-fluid" />
          </div>
          <div class="col-6">
            <!-- 2.รับค่าจาก emit @cc แล้วส่งไปทำงานใน function "sum"-->
            <emotion label @cc="sum" />
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <hr class="featurette-divider" />
      <div class="row featurette alert alert-success" style="opacity: 0.9; ">
        <div class="row align-items-center">
          <div class="col-6">
            <!-- 2.รับค่าจาก emit @cc แล้วส่งไปทำงานใน function "sum"-->
            <emotion label @cc="sum" />
          </div>
          <div class="col-6">
            <img :src="img[2].src" class="img-fluid" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import emotion from "./components/emotion.vue";
export default {
  name: "App",
  components: { emotion },
  data: function () {
    return {
      img: [
        {
          src:
            "https://discordapp.com/channels/746380296630567082/746380296630567085/746380470807167027",
        },
        {
          src:
            "https://discordapp.com/channels/746380296630567082/746380296630567085/746380478365565130",
        },
        {
          src:
            "https://discordapp.com/channels/746380296630567082/746380296630567085/746380485969575947",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: "Do Hyeon", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 60px;
}

</style>