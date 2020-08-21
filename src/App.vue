<template>
  <div id="app">
    <div class="container">      
      <div id="myCarousel" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
          <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
          <li data-target="#myCarousel" data-slide-to="1" class="active"></li>
          <li data-target="#myCarousel" data-slide-to="2" class="active"></li>
        </ol>
        <div class="carousel-inner">
          <div class="carousel-item">
            <img :src="img[0].src" height="500" width="700"/>
          </div>
          <div class="carousel-item active">
            <img :src="img[1].src" height="500" width="700"/>
          </div>
          <div class="carousel-item">
            <img :src="img[2].src" height="500" width="700"/>
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
      <div class="row featurette alert alert-danger" style="opacity: 1.0; ">
        <div class="row align-items-center">
          <div class="col-6">
            <img :src="img[0].src" class="img-fluid" />
          </div>
          <div class="col-6">
            <emotion label @cc="sum" />
          </div>          
        </div>
      </div>
    </div>
    <div class="container">
      <hr class="featurette-divider" />
      <div class="row featurette alert alert-info" style="opacity: 1.0; ">
        <div class="row align-items-center">
          <div class="col-6">
            <img :src="img[1].src" class="img-fluid" />
          </div>
          <div class="col-6">
            <emotion label @cc="sum" />
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <hr class="featurette-divider" />
      <div class="row featurette alert alert-danger" style="opacity: 1.0; ">
        <div class="row align-items-center">
          <div class="col-6">
            <img :src="img[2].src" class="img-fluid" />
          </div>
          <div class="col-6">
            <emotion label @cc="sum" />
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
          src: "https://cdn.discordapp.com/attachments/746380296630567085/746380470735994880/cat.jpg", },
        {
          src: "https://cdn.discordapp.com/attachments/746380296630567085/746380478059118682/panda.jpg", },
        {
          src: "https://cdn.discordapp.com/attachments/746380296630567085/746380486032752700/tiger.jpg", },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color:#2c3e50;
  margin-top: 100px;
}

</style>