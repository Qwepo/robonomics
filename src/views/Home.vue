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
          <h1 class="home__text"> Laboratory of Multi-Agent Systems in Smart Cities and Industry 4.0</h1>
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
  height: calc(100vh - 40px);
  margin: 0 400px;
}

.logo{
  width: 550px;
  margin: 30px;
}
.home__text {
  color: #fff;
  font-weight: 700;
  font-size: 30px;
}

/* Adaptation for smartphones */
/* Adaptation for 1200px */
@media screen and (max-width: 1200px) {
  .home{
    height: 100vh;
    overflow: hidden;
    position: relative;
  }
  .bckg{
    height: auto;
  }

}
@media (min-width: 1200px) {

  .home{
    height: auto;
    align-items: center;
  }
  .home__inner{
    margin-top: -50px;
    align-items: center;
    flex-direction: column;
  }
  .logo{
    width: 400px;
  }
  .home__text{
    text-align: center;
    font-size: 20px;
  }
}
@media screen and (min-width: 922px) and (max-width: 1199px) {
   .home{
    height: auto;
    align-items: center;
  }
}
@media screen and (min-width: 768px) and (max-width: 991px) {
  .home__inner{
    margin: 0 auto;
    flex-direction: column;
  }
  .logo{
    width: 250px;
  }
  .home__text{
    margin-bottom: 30px;
    text-align: center;
    font-size: 20px;
  }
}
@media screen and (max-width: 767px) {
  .bckg{
    height: 100vh;
    width: auto;
    position: absolute;
  }
  .home__inner{
   margin: 0;
    flex-direction: column;
    align-items: center;
  }
  .logo{
    width: 500px;
  }
  .home__text{
    text-align: center;
    font-size: 20px;
  }
}
@media screen and (max-width: 480px) {
  .bckg{
    height: 100%;
    width: auto;
  }
  .home{
    align-items: center;
    height: 100vh;
    width: 100%;
  }
  .home__inner{
    margin: 0;
    flex-direction: column;
    align-items: center;
  }
  .logo{
    width: 300px;
  }
  .home__text{
    text-align: center;
    font-size: 20px;
  }

}

</style>
