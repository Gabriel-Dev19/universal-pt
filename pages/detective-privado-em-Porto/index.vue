<template>
  <div>
    <Home
      name-btn="Veja as cidades"
      hash-btn="cidades"
      title-principal="Detective privado no distrito de Porto"
    />
    <div class="container container-text-cidades row mx-auto justify-content-center">
      <div class="col-10 px-0">
        <h2 class="azul mb-3 text-center">
          Encontre um detective em Porto
        </h2>
        <p class="text-center">
          A UNIVERSAL DETECTIVES está em Porto e desejamos ajudar você a solucionar suas dúvidas. Com <span class="P-negrito">mais de 20 anos de experiência</span> e centenas de casos solucionados, atuamos em todo o território nacional e países do Mercosul. Nosso principal objetivo é esclarecer as dúvidas de nossos clientes, antes de tomar uma atitude diante a situação em que você está vivenciando, é importante que você tenha plena certeza de tudo que está acontecendo.
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
              A
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Amarante">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Amarante
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
              F
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Felgueiras">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Felgueiras
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
              G
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Gondomar">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Gondomar
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
              L
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Lousada">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Lousada
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
              M
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Maia">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Maia
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="MarcoDeCanaveses">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Marco de Canaveses
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Matosinhos">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Matosinhos
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
              P
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="PacosDeFerreira">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Paços de Ferreira
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Paredes">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Paredes
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Penafiel">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Penafiel
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Porto">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Porto
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="PovoaDeVarzim">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Póvoa de Varzim
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="SantaMariaDaFeira">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Santa Maria da Feira
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="SantoTirso">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Santo Tirso
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
              V
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Valongo">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Valongo
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="VilaDoConde">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Vila do Conde
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="VilaNovaDeGaia">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Vila Nova de Gaia
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
    title: 'Detective privado em Porto - Universal Detectives Privados'
  },
  methods: {
    Amarante () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Amarante/')
    },
    Felgueiras () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Felgueiras/')
    },
    Gondomar () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Gondomar/')
    },
    Lousada () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Lousada/')
    },
    Maia () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Maia/')
    },
    MarcoDeCanaveses () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Marco-de-Canaveses/')
    },
    Matosinhos () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Matosinhos/')
    },
    PacosDeFerreira () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Pacos-de-Ferreira/')
    },
    Paredes () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Paredes/')
    },
    Penafiel () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Penafiel/')
    },
    Porto () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Porto/')
    },
    PovoaDeVarzim () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Povoa-de-Varzim/')
    },
    SantaMariaDaFeira () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Santa-Maria-da-Feira/')
    },
    SantoTirso () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Santo-Tirso/')
    },
    Valongo () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Valongo/')
    },
    VilaDoConde () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Vila-do-Conde/')
    },
    VilaNovaDeGaia () {
      this.$router.push('/detective-privado-em-Porto/detective-privado-em-Vila-Nova-de-Gaia/')
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
