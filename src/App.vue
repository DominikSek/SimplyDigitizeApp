<template>
  <div class="navigation">
    <nav class="navbar">
      <div class="left">
        <img class="navbar-img-fer" src="../src/img/fer.png" alt="FER">
      </div>
      <router-link to="/" class="navbar-brand" >
        <img class="navbar-img" src="../src/img/logo.png" alt="Logo">
      </router-link>
      <div class="right">
        <p class="nav-gallery"> 2022. </p>
      </div>
    </nav>
  </div>
  <br>

  <router-view/>


</template>



<style>

  body {

    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;

  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .navbar-brand{
    width: 33%;
  }
  .icon-img {

    max-width: 200px;
    max-height: 200px;
  }
  .nav-gallery{
    text-align: center;

    font-family: Avenir, Helvetica, Arial, sans-serif;
    font-size: 3rem;
    color: #000000;
    margin: 1.5rem 0 0 1rem;
    padding-left: 7rem;

  }
  .right{
    width: 33%;
    float:right;
    display: inline-block;
    margin-top: 1rem;
    font-weight: bold;
    position: relative;

  }
  .left{
    width: 33%;
    float:left;
    display: inline-block;
    font-weight: bold;
    padding: 0;
    margin-top: 0.5em;
  }
  .navbar-img-fer{
    max-width: 300px;
    max-height: 200px;

  }

</style>
