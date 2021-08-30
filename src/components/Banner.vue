<template>
  <div class="banner">
    <section class="hero banner__hero is-halfheight">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-7">
              <h1 class="title is-size-1 mb-6 has-text-white">
                A vitrine para soluções e tecnologias inovadoras em mineração
              </h1>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";

.banner {
  background: no-repeat right bottom;
  background-size: cover;
}

.banner__hero .title,
.subtitle {
  text-shadow: $baseShadow;
}

.banner__hero {
  background: rgba($color: #000, $alpha: 0.4);
  height: 645px;
}
</style>

<script>
export default {
  name: "banner",
  data() {
    return {
      heroSize: "",
      backGroundImage: "",
    };
  },
};
</script>
