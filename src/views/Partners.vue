<template>
  <div class="partners">
    <!-- begin: Partners -->
    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>
        </div>
        <div class="columns my-6">
          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>

          <div class="column is-3">
            <figure class="image">
              <img class="is-rounded" src="https://via.placeholder.com/150" />
            </figure>
          </div>
        </div>
      </div>
    </section>
    <!-- end: Partners -->

    <!-- begin: Content section -->
    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-6 is-offset-3">
            <h3
              class="title is-size-3 has-text-weight-normal has-text-centered"
            >
              Alberding
            </h3>
            <p>
              A InnovBrazil é uma empresa de consultoria sediada em Belém
              fundada em maio de 2016 pelo Dr. Bertram Heinze, geólogo com mais
              de 15 anos de experiência na área de Transferência Internacional
              de Tecnologia e Gestão de Relações Externas para os setores
              público e privado na Alemanha, Rússia e Brasil.A InnovBrazil
              desenvolveu conhecimento especializado do mercado de mineração do
              Norte do Brasil e estabeleceu uma ampla rede com empresas de
              mineração e logística mineral ativas na região.
            </p>
          </div>
        </div>
        <div class="columns mt-6">
          <div class="column is-8 is-offset-2">
            <figure>
              <img src="https://via.placeholder.com/1000x620" alt="" />
            </figure>
            <div class="colums is-centered">
              <div class="column">
                <div class="has-text-centered mt-6">
                  <a href="#" class="button is-info">Saiba mais</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- end: Content section -->
  </div>
</template>

<script>
export default {
  name: "Partners",
  methods: {
    changeNavbarModifier() {
      const navbar = document.getElementById("nav");
      const navbarBrandImages = navbar.querySelectorAll(".navbar-brand img");
      console.log();
      navbar.querySelector('.navbar').classList.remove('is-dark')

      for (const image of navbarBrandImages) {
        image.classList.toggle('is-hidden');
      }
      
      
    },
  },
  mounted() {
    this.changeNavbarModifier();
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";
.partners {
  margin-top: 5rem;
  margin-bottom: 5rem;
}

.partners .image img {
  width: 185px;
}
</style>
