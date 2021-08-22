<template>
  <div class="carousel">
    <section class="hero carousel__hero is-fullheight-with-navbar">
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
export default {
  name: "Carousel",
  data() {
    return {
      heroSize: "",
    };
  },
};
</script>
