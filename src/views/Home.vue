<template>
  <div class="home">
    <Carousel />
    <Partners />

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
</style>
