<template>
  <div :class="{ 'container': true, 'background': background }">
    <div class="nav">
      <a href="#" class="nav__link">About us</a>
      <a href="#" class="nav__link">Job</a>
      <a href="#" class="nav__link">Contacts</a>
      <a href="#" class="nav__link">English</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'headers',
  props: {
    background: {
      type: Boolean, default: false
    }
  }
}

</script>

<style>
.container.background {
  background: #000;
}

.nav{
  min-height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 5;
}
.nav__link{
  margin: 0 15px;
  padding: 5px;

  text-decoration: none;
  text-transform: uppercase;
  font-weight: 700;
  color: #fff;

  border-radius: 5%;
  transition: background-color 0.1s linear;

}
.nav__link:hover {
  background-color: red;
}
.container{
  width: 100%;;
}

@media screen and (max-width: 1200px) {
  .nav__link{
    margin: 0 2%;

    font-size: 15px;
  }
}
</style>
