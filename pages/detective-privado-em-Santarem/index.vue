<template>
  <div>
    <Home
      name-btn="Veja as cidades"
      hash-btn="cidades"
      title-principal="Detective privado no distrito de Santarém"
    />
    <div class="container container-text-cidades row mx-auto justify-content-center">
      <div class="col-10 px-0">
        <h2 class="azul mb-3 text-center">
          Encontre um detective em Santarém
        </h2>
        <p class="text-center">
          A UNIVERSAL DETECTIVES está em Santarém e desejamos ajudar você a solucionar suas dúvidas. Com <span class="P-negrito">mais de 20 anos de experiência</span> e centenas de casos solucionados, atuamos em todo o território nacional e países do Mercosul. Nosso principal objetivo é esclarecer as dúvidas de nossos clientes, antes de tomar uma atitude diante a situação em que você está vivenciando, é importante que você tenha plena certeza de tudo que está acontecendo.
        </p>
        <p class="text-center">
          Nossa agência é especializada em investigações de caráter conjugal, industrial, empresarial, comercial, familiar, política e assuntos privados. Seja qual for a complexidade dos desafios que você vêm enfrentando, a UNIVERSAL DETECTIVES terá a satisfação em ajuda-lo a desvendar o seu caso.
        </p>
        <h2 id="cidades" class="azul text-center">
          Confira as cidades atendidas
        </h2>
      </div>
    </div>
    <section class="col-12 mt-50 px-0">
      <div class="container px-xs-0">
        <!-- Cidades G -->
        <div class="position-relative bg-roxo-escuro border shadow bg-azul-caixa-cidade mt-30 overflow-hidden col-12 d-flex row mx-auto pr-0 pt-1 pb-30 pl-65">
          <div class="d-flex div-bolinha-letra-cidade justify-content-center align-items-center">
            <h5 class="fw-700 mb-0">
              O
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Ourem">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Ourém
          </a>
        </div>
      </div>
    </section>
    <section class="col-12 mt-50 px-0">
      <div class="container px-xs-0">
        <!-- Cidades G -->
        <div class="position-relative bg-roxo-escuro border shadow bg-azul-caixa-cidade mt-30 overflow-hidden col-12 d-flex row mx-auto pr-0 pt-1 pb-30 pl-65">
          <div class="d-flex div-bolinha-letra-cidade justify-content-center align-items-center">
            <h5 class="fw-700 mb-0">
              S
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Santarem">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Santarém
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
    title: 'Detective privado em Santarém - Universal Detectives Privados'
  },
  methods: {
    Ourem () {
      this.$router.push('/detective-privado-em-Santarem/detective-privado-em-Ourem/')
    },
    Santarem () {
      this.$router.push('/detective-privado-em-Santarem/detective-privado-em-Santarem/')
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
  .P-negrito {
    font-weight: 600;
  }
</style>
