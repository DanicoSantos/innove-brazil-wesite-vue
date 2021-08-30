<template>
  <div class="about">
    <Banner />

    <!-- begin:About Innov Brazil text -->
    <section class="section mt-6">
      <div class="container">
        <div class="columns">
          <div class="column is-8 is-offset-2">
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
            <p class="title is-size-3 has-text-centered my-6">
              “Somos uma empresa familiar.”
            </p>
            <p>
              A InnovBrazil busca se tornar a referência número um em soluções
              inovadoras para a indústria de mineração no Norte do Brasil. Nosso
              foco está no Estado do Pará, onde grandes investimentos em novos
              projetos de mineração estão acontecendo agora. O Pará combina um
              vasto território com as infra-estruturas existentes - estradas,
              portos, ferrovias, linhas de transmissão e centros populacionais.
              A InnovBrazil desenvolve esse mercado para você!
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- end:About Innov Brazil text -->

    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-4 is-offset-1">
            <figure class="image about__image">
              <img
                src="https://via.placeholder.com/400x600"
                alt="Maquinaria de mineração"
              />
            </figure>
          </div>
          <div class="column is-6">
            <div class="about__content pl-6">
              <p class="title is-size-2 has-text-weight-normal">
                Bertram Heinze (Ph.D.), alemão, geólogo por formação, com 15
                anos de experiência em relações externas para o setor público de
                pesquisa e a indústria de mineração privada.
              </p>
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
