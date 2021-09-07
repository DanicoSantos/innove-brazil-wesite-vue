<template>
  <div class="carousel">
    <section class="hero carousel__hero is-fullheight">
      <div id="carousel" class="hero-carousel">
        <div class="item-1">
          <img src="https://via.placeholder.com/1920x720" alt="" />
        </div>
        <div class="item-2">
          <!-- Slide Content -->
          <img src="https://via.placeholder.com/1920x720" alt="" />
        </div>
        <div class="item-3">
          <!-- Slide Content -->
          <img src="https://via.placeholder.com/1920x720" alt="" />
        </div>
      </div>
      <div class="hero-body">
        <div class="columns">
          <div class="column is-7">
            <h1 class="title is-size-1 mb-6 has-text-white">
              Somos especialistas no mercado de mineração
            </h1>
            <p class="subtitle has-text-white">
              A InnovBrazil desenvolveu conhecimento especializado do mercado de
              mineração do Norte do Brasil
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";
@import "../../node_modules/bulma-carousel";


.carousel {
  background: url(../assets/img/banner-home.jpg) no-repeat;
  background-size: cover;
}

.carousel__hero .title,
.subtitle {
  text-shadow: $baseShadow;
}

.carousel__hero {
  background: rgba($color: #000, $alpha: 0.4);
  height: 645px;
}
</style>

<script>
import bulmaCarousel from 'bulma-carousel'

export default {
  name: "Carousel",
  data() {
    return {
      heroSize: "",
    };
  },
  methods: {
    attachCarousel() {
      bulmaCarousel.attach('#carousel', {
				slidesToScroll: 1,
				slidesToShow: 4
			});
    }
  },
  created() {
    this.attachCarousel();
  }
};
</script>
