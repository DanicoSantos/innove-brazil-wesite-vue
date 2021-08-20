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
              <img src="https://via.placeholder.com/400x500" alt="" />
            </figure>
          </div>
          <div class="column is-6">
            <div class="about__content pl-6">
              <h2 class="title is-3">
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
        <h2
          class="title is-size-3 has-text-centered has-text-danger mb-6 services__title"
        >
          Serviços
        </h2>
        <div class="columns">
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img src="https://via.placeholder.com/80" alt="" />
              <p>Representação de vendas</p>
            </div>
          </div>
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img src="https://via.placeholder.com/80" alt="" />
              <p>Representação de vendas</p>
            </div>
          </div>
          <div class="column is-4">
            <div class="services__item has-text-centered">
              <img src="https://via.placeholder.com/80" alt="" />
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
    <section class="highlight mt-6">
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
              <h4 class="title is-size-4">Contato</h4>
              <address class="contact__address">
                <strong>Edifício Empresarial Bolonha</strong> <br />
                Av. José Malcher, 168, sala 110
              </address>
              <p class="contact__phone">
                +55 (91) 98111-1762
              </p>
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
};
</script>

<style scoped>
.about__content {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: flex-start;
  height: 80%;
}

.contact__info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 90%;
}
</style>
