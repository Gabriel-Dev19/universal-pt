<template>
  <div>
    <Home
      name-btn="Veja as cidades"
      hash-btn="cidades"
      title-principal="Detetive particular no Distrito Federal"
    />
    <div class="container container-text-cidades row mx-auto justify-content-center">
      <div class="col-10 px-0">
        <h2 class="azul mb-3 text-center">
          Encontre um detetive no Distrito Federal
        </h2>
        <p class="text-center">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit blanditiis, minus tempora porro
          vero quos voluptatem velit quae facere quis dolorem quod iste, itaque sequi corporis dolores
          tempore accusantium voluptatum!
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit blanditiis, minus tempora porro
          vero quos voluptatem velit quae facere quis dolorem quod iste, itaque sequi corporis dolores
          tempore accusantium voluptatum!
        </p>
        <h2 id="cidades" class="azul text-center">
          Confira as cidades atendidas
        </h2>
      </div>
    </div>
    <section class="col-12 mt-50 px-0">
      <div class="container px-xs-0">
        <!-- Cidades B -->
        <div class="position-relative bg-roxo-escuro border shadow bg-azul-caixa-cidade mt-30 overflow-hidden col-12 d-flex row mx-auto pr-0 pt-1 pb-30 pl-65">
          <div class="d-flex div-bolinha-letra-cidade justify-content-center align-items-center">
            <h5 class="fw-700 mb-0">
              B
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Brasilia">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Brasília – DF
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular no Distrito Federal - Universal Detetives Particulares'
  },
  methods: {
    Brasilia () {
      this.$router.push('/detetive-particular-no-Distrito-Federal/detetive-particular-em-Brasilia-DF/')
    }
  }
}
</script>
<style scoped>
  .separation-tema{
    position: absolute;
    height: 3px;
    width: 200px;
    bottom: -10px;
    border-radius: 3px;
    background-color: var(--roxo_escuro);
  }
  .borda-tema-fina{
    position: absolute;
    height: 2px;
    width: 200px;
    bottom: -1px;
    border-radius: 3px;
    background-color: var(--roxo_escuro);
  }
  .container-text-cidades{
    padding-top: 100px;
  }
  ol.carousel-indicators li{
    width: 13px !important;
    height: 13px !important;
  }
</style>
