<template>
  <div class="about">
    <Banner />
    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-5">
            <figure class="image about__image">
              <img
                src="@/assets/img/img-about.jpg"
                alt="Maquinaria de mineração"
              />
            </figure>
          </div>
          <div class="column is-5">
            <div class="about__content pl-6">
              <h2 class="title is-3 title--special">
                Especialista no mercado de mineração
              </h2>
              <p class="subtitle is-4">
                A InnovBrazil é uma empresa de consultoria sediada em Belém
              </p>
              <p class="about__text">
                A InnovBrazil desenvolveu conhecimento especializado do mercado
                de mineração do Norte do Brasil e estabeleceu uma ampla rede com
                empresas de mineração e logística mineral ativas na região.
              </p>
              <button class="button is-info">Conheça</button>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
export default {
  name: "About",
  components: {
    Banner,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";

.about__content {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
  height: 80%;
  color: $primaryColor;
}

.about__content .title,
.subtitle {
  color: $primaryColor;
}

.about .image img {
  position: relative;
  z-index: 10009;
}

.about__image::after {
  content: "";
  border: 3px solid $primaryColor;
  position: absolute;
  top: 3%;
  left: 3%;
  width: 100%;
  height: 100%;
  z-index: 10000;
}
</style>
