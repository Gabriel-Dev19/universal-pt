<template>
  <div>
    <Home
      name-btn="Veja as cidades"
      hash-btn="cidades"
      title-principal="Detective privado no distrito de Lisboa"
    />
    <div class="container container-text-cidades row mx-auto justify-content-center">
      <div class="col-10 px-0">
        <h2 class="azul mb-3 text-center">
          Encontre um detective em Lisboa
        </h2>
        <p class="text-center">
          A UNIVERSAL DETECTIVES está em Lisboa e desejamos ajudar você a solucionar suas dúvidas. Com <span class="P-negrito">mais de 20 anos de experiência</span> e centenas de casos solucionados, atuamos em todo o território nacional e países do Mercosul. Nosso principal objetivo é esclarecer as dúvidas de nossos clientes, antes de tomar uma atitude diante a situação em que você está vivenciando, é importante que você tenha plena certeza de tudo que está acontecendo.
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Alcobaca">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Alcobaça
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Alenquer">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Alenquer
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Almada">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Almada
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Amadora">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Amadora
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
              B
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Barreiro">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Barreiro
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
              C
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Cascaes">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Cascaes
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Lisboa">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Lisboa
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Loures">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Loures
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Mafra">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Mafra
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Moita">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Moita
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Montijo">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Montijo
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
              O
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Odivelas">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Odivelas
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Oeiras">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Oeiras
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Palmela">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Palmela
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Sesimbra">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Sesimbra
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Setubal">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Setúbal
          </a>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="Sintra">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Sintra
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
              T
            </h5>
          </div>
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="TorresVedras">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Torres Vedras
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
          <a class="d-flex col-12 mt-4 px-0 py-0 text-preto-cidades fs-sm-18 fw-600 btn align-items-center" @click.prevent="VilaFrancaDeXira">
            <ion-icon class="fs-20 text-vermelho mr-2" name="navigate-circle-outline" /> Vila Franca de Xira
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
    title: 'Detective privado em Lisboa - Universal Detectives Privados'
  },
  methods: {
    Alcobaca () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Alcobaca/')
    },
    Alenquer () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Alenquer/')
    },
    Almada () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Almada/')
    },
    Amadora () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Amadora/')
    },
    Barreiro () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Barreiro/')
    },
    Cascaes () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Cascaes/')
    },
    Lisboa () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Lisboa/')
    },
    Loures () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Loures/')
    },
    Mafra () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Mafra/')
    },
    Moita () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Moita/')
    },
    Montijo () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Montijo/')
    },
    Odivelas () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Odivelas/')
    },
    Oeiras () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Oeiras/')
    },
    Palmela () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Palmela/')
    },
    Santarem () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Santarem/')
    },
    Sesimbra () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Sesimbra/')
    },
    Setubal () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Setubal/')
    },
    Sintra () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Sintra/')
    },
    TorresVedras () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Torres-Vedras/')
    },
    VilaFrancaDeXira () {
      this.$router.push('/detective-privado-em-Lisboa/detective-privado-em-Vila-Franca-de-Xira/')
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
