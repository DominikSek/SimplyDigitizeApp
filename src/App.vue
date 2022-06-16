<template>
  <div class="navigation">
    <nav class="navbar navbar-default">
      <div class="left">
        <img class="navbar-img-fer" src="../src/img/fer.png" alt="FER">
      </div>
      <router-link to="/" class="navbar-brand" >
        <img class="navbar-img" src="../src/img/logo.png" alt="Logo">
      </router-link>
      <div class="right">
        <p class="nav-gallery"> Model Gallery </p>
      </div>
    </nav>
  </div>
  <br>

  <router-view/>
</template>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .icon-img {

    max-width: 200px;
    max-height: 200px;
  }
  .nav-gallery{
    text-align: right;
    justify-content: end;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    font-size: 2rem;


  }
  .right{
    float:right;
    display: inline-block;
    margin: 0.8em 1em 1em 1em;
    font-weight: bold;
  }
  .left{
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
