<template>
  <div class="container">
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
  props: ['background']
}

</script>

<style>
.nav{
  min-height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: var(--background);
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

@media screen and (max-width: 1000px) {
  .nav__link{
    margin: 0 auto;
  }
}
</style>
