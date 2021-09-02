<template>
  <div class="services">
    <!-- begin: Banner -->
    <div class="banner__background-image">
      <Banner title="Nossos serviços" />
    </div>
    <!-- begin: Banner -->

    <!-- begin: Services -->
    <section class="section mt-5 services__items">
      <div class="container mb-6 services--sales-rep">
        <h3 class="title is-size-3 has-text-weight-normal">
          Representação de vendas
        </h3>
        <div class="columns">
          <div class="column services__items-text is-4">
            <p>
              Desenvolvimento de relações comerciais com clientes e parcerias de
              cooperação tecnológica.
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Realização de estudos de mercado para clientes e segmentos de
              tecnologia específicos.
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Análise do potencial de mercado para novas tecnologias e soluções.
            </p>
          </div>
        </div>
      </div>

      <div class="container mb-5 services--market-dev">
        <h3 class="title is-size-3 has-text-weight-normal">
          Desenvolvimento de mercado
        </h3>
        <div class="columns">
          <div class="column services__items-text is-4">
            <p>
              Conexão de empresas europeias com a indústria de mineração e
              minerais no Estado do Pará.
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Representação de vendas internacionais para fabricantes de
              equipamentos de mineração e processamento mineral no Norte do
              Brasil.
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Promoção de soluções inovadoras e econômicas para mineração e
              indústria no Brasil.
            </p>
          </div>
        </div>
      </div>

      <div class="container mb-5 services--project-man">
        <h3 class="title is-size-3 has-text-weight-normal">
          Gerenciamento de progetos
        </h3>
        <div class="columns">
          <div class="column services__items-text is-4">
            <p>
              Gerenciamento de projetos de cooperação internacional por meio de
              monitoramento de progresso personalizado
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Preparação de pedidos de financiamento em conjunto com parceiros
              locais e internacionais.
            </p>
          </div>
          <div class="column services__items-text is-4">
            <p>
              Relatórios financeiros e técnicos em inglês, alemão ou português.
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- end: Services -->

    <!-- begin: Contact -->
    <section class="section pt-0">
      <div class="container">
        <div class="columns">
          <div class="column is-8 is-offset-2 has-text-centered">
            <button class="button is-danger">Conheça</button>
          </div>
        </div>
      </div>
    </section>
    <!-- end: Languages -->
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
export default {
  name: "Services",
  components: {
    Banner,
  },
  methods: {
    changeNavbarOnScroll() {
      const navbar = document.getElementById("nav");

      if (
        document.body.scrollTop > 20 ||
        document.documentElement.scrollTop > 20
      ) {
        navbar.querySelector(".navbar").classList.remove("is-dark");
      } else {
        navbar.querySelector(".navbar").classList.add("is-dark");
      }
    },
  },
  created() {
    window.onscroll = () => {
      this.changeNavbarOnScroll();
    };

    document.querySelector(".navbar").classList.add("is-dark");
  },
  beforeUnmount() {
    window.onscroll = () => null;
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";
@import "../../node_modules/bulma-divider";

.banner__background-image {
  background-image: url("../assets/img/banner-services.jpg");
}

.services__content {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
  height: 80%;
  color: $primaryColor;
}

// Services items

.services__items .title {
  position: relative;
}

.services__items .title::before {
  content: "";
  display: block;
  background-repeat: no-repeat;
  background-size: contain;
  width: 85px;
  height: 85px;
  margin-left: 0.5rem;
}

.services__items-text::before {
  content: "";
  display: block;
  width: 1.5rem;
  height: 0.3rem;
  border-top: 0.2rem solid $dangerColor;
}

.services__items-text {
  font-size: 1.2rem;
  font-weight: 400;
  color: $grey;
}

.services__items .services--sales-rep .title::before {
  background-image: url("../assets/img/icons/holding-hands.svg");
}

.services__items .services--market-dev .title::before {
  background-image: url("../assets/img/icons/marketing-charts.svg");
  width: 65px;
  height: 65px;
  margin-bottom: 0.8rem;
  margin-left: 0.8rem;
}

.services__items .services--project-man .title::before {
  background-image: url("../assets/img/icons/cog-charts.svg");
  width: 65px;
  height: 65px;
  margin-bottom: 0.5rem;
}
</style>
