<template>
  <div class="home">
    <Carousel />
    <Partners />
    <!-- begin: About section -->
    <section class="section about">
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
    <!-- end: About section -->

    <!-- begin: Services section -->
    <section class="section services">
      <div class="container">
        <div class="services__title">
          <h2
            class="
              title title--special
              is-uppercase is-size-3
              has-text-danger
              mb-6
            "
          >
            Serviços
          </h2>
        </div>
        <div class="columns">
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img
                src="@/assets/img/icons/holding-hands.svg"
                width="149"
                alt=""
              />
              <p>Representação de vendas</p>
            </div>
          </div>
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img
                src="@/assets/img/icons/marketing-charts.svg"
                width="115"
                alt=""
              />
              <p>Desenvolvimento de mercado</p>
            </div>
          </div>
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img src="@/assets/img/icons/cog-charts.svg" width="123" alt="" />
              <p>Representação de vendas</p>
            </div>
          </div>
        </div>
        <div class="has-text-centered mt-6">
          <button class="button is-danger">Saiba mais</button>
        </div>
      </div>
    </section>
    <!-- end: Services section -->

    <!-- begin: Highlight section -->
    <section class="section highlight mt-6">
      <div class="container">
        <div class="columns">
          <div class="column is-4">
            <img src="https://via.placeholder.com/400" alt="" />
          </div>
          <div class="column is-4">
            <img src="https://via.placeholder.com/400" alt="" />
          </div>
          <div class="column is-4">
            <img src="https://via.placeholder.com/400" alt="" />
          </div>
        </div>
      </div>
    </section>
    <!-- end: Highlight section -->

    <!-- begin: Contact section -->
    <section class="section contact mt-6">
      <div class="container">
        <div class="columns">
          <div class="column is-6">
            <img src="https://via.placeholder.com/600x470" alt="" />
          </div>
          <div class="column p-6">
            <div class="contact__info">
              <h4 class="title is-size-4 is-uppercase">Contato</h4>
              <address class="contact__address">
                <strong>Edifício Empresarial Bolonha</strong> <br />
                Av. José Malcher, 168, sala 110
              </address>
              <p class="contact__phone">+55 (91) 98111-1762</p>
              <p class="contact__email">Bertram.heinze@innovbrazil.com</p>
              <p class="contact__working-hours">
                Segunda a sexta, das 9h às 18h
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- end: Contact section -->
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "@/components/Carousel";
import Partners from "@/components/Partners";

export default {
  name: "Home",
  components: {
    Carousel,
    Partners,
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
    window.onscroll = () => null
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";

// About section
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

// Services section
.services .services__title {
  display: flex;
  justify-content: center;
  margin: 1rem auto;
}

.services .title--special::after {
  border-color: $dangerColor;
  text-align: center;
  width: 20%;
}

.services__item {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  height: 100%;
}

.services .button.is-danger {
  background-color: $dangerColor;
}

// Contact section
.contact__info .title,
.subtitle,
address,
strong,
p {
  color: $primaryColor;
}

.contact__info .title {
  font-weight: 400;
}

.contact__info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 90%;
}

/* Helpers */
.title--special {
  position: relative;
  font-weight: 400;
}

.title--special::after {
  content: "";
  position: absolute;
  bottom: -20%;
  left: 0;
  border-bottom: 3px solid $primaryColor;
  width: 5%;
}
</style>
