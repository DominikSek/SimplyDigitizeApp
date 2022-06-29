<template>
  <div class="scrollblock">
      <div class="row">
          <div class="card-columns">
            <div class="card card-hover" v-for="item in models">
              <div class="card-body">
                <router-link :to="'/'+ item.model">
                  <img class="card-img-top" src="../img/teddy_bear.jpeg" alt="Card image cap">
                  <div class="reveal ">
                    <div class="align-self-center">
                      <p> {{item.text}}</p>
                    </div>
                  </div>
                </router-link>
              </div>
            </div>
          </div>
      </div>
  </div>

</template>

<script>
  export default {
    name: 'HomeView',
    data(){
      return {
        numbers: 6,
        models: [
          {
            model: "model-1",
            text: "Medvjedić Lovro"
          },
          {
            model: "model-2",
            text: "Morska kornjača Dominik"
          },
          {
            model: "model-3",
            text: "Jelen Jelena"
          },
          {
            model: "model-4",
            text: "Ljetni šeširić"
          },
          {
            model: "model-5",
            text: "Meduza Mirta"
          },
          {
            model: "model-6",
            text: "Medvjedić Matko"
          },

        ]
      }
    }
  }

</script>



<style>
  a:link,
  a:hover,
  a:visited {
    text-decoration: none;
    color: #000;
  }

  a:link .white,
  a:hover .white,
  a:visited .white {
    text-decoration: none;
    color: #fff;
  }


  .container a {
    display: inline-block;
    position: relative;
    text-align: center;
    color: #000;
    text-decoration: none;
    font-size: 20px;
    overflow: hidden;
    top: 5px;
  }

  .container a:after {
    content: '';
    position: absolute;
    background: #000;
    height: 2px;
    width: 0%;
    transform: translateX(-50%);
    left: 50%;
    bottom: 0;
    transition: .35s ease;
  }

  .container a:hover:after,
  .container a:focus:after,
  .container a:active:after {
    width: 100%;
  }


  @media (max-width: 767px) {
    h1 {
      font-size: 2.5rem;
    }
    .button_container.active {
      right: 15px;
    }
  }

  .card {
    border: 0;
    border-radius: 0;


  }

  .card-img,
  .card-img-top {
    padding-top: 10px;
    max-height: 20rem;
    border-radius : 10%;
    position: inherit;
  }

  .card-body {
    padding-bottom: 0;
    background-color: rgba(255, 244, 213, 0.25);
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    border-radius: 10%;
    justify-content: center;

  }
  .card-body:hover {
    box-shadow: 0 20px 20px 0 rgba(0, 0, 0, 0.2), 0 10px 30px 0 rgba(0, 0, 0, 0.19);
    background-color: rgba(221, 221, 221, 0.69);
  }



  @media (max-width: 991px) {
    .card-columns {
      column-count: 1;
    }
  }

  @media (min-width: 992px) {
    .card-columns {
      column-count: 2;
    }
  }

  @media (min-width: 1200px) {
    .card-columns {
      column-count: 3;
    }
  }



  .reveal p {
    line-height: 100%;
    font-size: 1.25rem;
    text-align: center;
    border-radius: 10%;
      padding: 5px;
  }

  .card-hover .reveal {
    visibility: hidden;


  }

  .card-hover:hover .reveal {
    height: auto;
    visibility: visible;
    opacity: 0.5;
    transition: opacity 1s ease;
    position: page;
    width: 100%;
    top: 0;
    background-color: #dc6e1f;
    color: white;
    border-radius: 20px;
    margin: 0;

  }

</style>
