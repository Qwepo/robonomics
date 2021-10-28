<template>
  <div class="home">
    <div class="video">
      <video src="../assets/home.webm" class="bckg" autoplay muted loop></video>
    </div>
    <div class="home__content">
            <headers/>
      <div class="container">
        <div class="home__inner">
          <img src="../assets/logo.png" alt="" class="logo">
          <h1> Laboratory of Multi-Agent Systems in Smart Cities and Industry 4.0</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import headers from '../components/headers.vue'
export default {
  name: 'Home',
  components: {
    headers
  }
}
</script>

<style scoped>
.home{
  max-height: 100vh;
  overflow: hidden;
  position: relative;

}
.video{
  padding-bottom: 52%;
}
.home::after{
  content: "";
  display: block;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
}
.bckg {
  height: auto;
  width: 100%;

  position: absolute;
  top: 0;
  left: 0;
}
.home__content {
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 3;
}
.home__inner{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
.logo{
  width: 30%;
  margin: 30px;
}
.home__text {
  color: #fff;
  font-weight: 400;
  font-size: 20px;
}

</style>
