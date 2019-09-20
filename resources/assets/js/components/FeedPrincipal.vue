<template>
  <div>
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img class="d-block w-100" v-bind:src="getImage(lista[0].path_image)" alt="Slide" />
          <div class="carousel-caption d-none d-md-block ">
            <h5>{{lista[0].titulo}}</h5>
            <p>{{lista[0].descricao}}</p>
          </div>
        </div>
        <div class="carousel-item">
          <img class="d-block w-100" v-bind:src="getImage(lista[1].path_image)" alt="Slide" />
          <div class="carousel-caption d-none d-md-block ">
            <h5>{{lista[1].titulo}}</h5>
            <p>{{lista[1].descricao}}</p>
          </div>
        </div>
        <div class="carousel-item">
          <img class="d-block w-100" v-bind:src="getImage(lista[5].path_image)" alt="Slide" />
          <div class="carousel-caption d-none d-md-block ">
            <h5>{{lista[5].titulo}}</h5>
            <p>{{lista[5].descricao}}</p>
          </div>
        </div>
      </div>
      <a
        class="carousel-control-prev"
        href="#carouselExampleIndicators"
        role="button"
        data-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a
        class="carousel-control-next"
        href="#carouselExampleIndicators"
        role="button"
        data-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: ["lista"],
  methods: {
    getImage: function(url) {
      return require("../../img/" + url + ".jpg");
    }
  }
};
</script>
