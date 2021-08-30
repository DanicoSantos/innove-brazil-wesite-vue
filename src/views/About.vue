<template>
  <div class="about">
    <div class="banner__background-image">
      <Banner
        title="A vitrine para soluções e tecnologias inovadoras em mineração"
      />
    </div>
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

    <!-- begin: Media section -->
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
    <!-- end: Media section -->

    <!-- begin: About Innov Brazil text part ii -->
    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-8 is-offset-2">
            <p>
              Criou e atuou como diretor do Helmholtz Office Moscow e da Casa
              Alemã de Ciência e Inovação, São Paulo (@AHK São Paulo); De 2011 a
              2016 constituiu e chefiou o Departamento de Relações Externas e
              Projetos de Pesquisa do Instituto Tecnológico Vale em Belém, Pará,
              Brasil.
            </p>
            <p class="mt-6">
              Em 2016 Bertram fundou a InnovBrazil com foco no desenvolvimento
              de novas oportunidades de negócios para empresas europeias no
              Norte do Brasil, o pólo de mineração de mais rápido crescimento na
              América Latina, com grandes reservas em Fe, Al, Cu, Ni, Mn, P
              ;&amp; Au; expansão rápida das instalações portuárias para
              exportação de minerais e grãos e importação de fertilizantes,
              carvão de coque e clinquer.
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- end: About Innov Brazil text part ii -->

    <!-- begin: Divider -->
    <div class="section py-0">
      <div class="container">
        <div class="columns">
          <div class="column is-1 is-offset-6">
            <div class="custom-divider mb-0"></div>
          </div>
        </div>
      </div>
    </div>
    <!-- end: Divider -->]
    <!-- begin: Languages -->
    <section class="section pt-0">
      <div class="container">
        <div class="columns">
          <div class="column is-8 is-offset-2 has-text-centered">
            <p class="title is-size-4 has-text-weight-normal">
              Oferecemos serviços em inglês, português e alemão.
            </p>
            <div
              class="has-text-centered mb-6 is-flex is-align-items-center is-justify-content-center"
            >
              <span>
                <img
                  src="@/assets/img/icons/flag-for-united-states.svg"
                  alt=""
                />
              </span>
              <span class="px-6">
                <img src="@/assets/img/icons/flag-for-brazil.svg" alt="" />
              </span>
              <span>
                <img src="@/assets/img/icons/flag-for-germany.svg" alt="" />
              </span>
            </div>
            <button class="button is-info">Conheça</button>
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
  name: "About",
  components: {
    Banner,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables.scss";
@import "../../node_modules/bulma-divider";

.banner__background-image {
  background-image: url("../assets/img/banner-about.jpg");
}

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
.custom-divider {
  display: block;
  position: relative;
  border-top: $divider-thickness solid $divider-color;
  height: 0.1rem;
  margin: 2rem 0;
  text-align: center;
  width: 80%;
}
</style>
