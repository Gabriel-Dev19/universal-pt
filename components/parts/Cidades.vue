<template>
  <div>
    <Home
      name-btn="Saiba mais"
      hash-btn="sobre"
      :title-principal="`Detective privado em ${nameCidades}`"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../assets/img/detetive-lupa.webp')"
        title-badge="sobre nós"
        parte-azul="Encontre detectives em:"
        :title-header="nameCidades"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Atuamos a mais de 20 anos em todo o território nacional além de diversos países do mercosul, solucionando casos de qualquer que seja a complexidade e ajudando a esclarecer todas as dúvidas dos nossos clientes."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          Detectives Privados em {{ nameCidades }}
        </h2>
        <p>
          A UNIVERSAL DETECTIVES está em <span class="P-negrito"> {{ nameCidades }} </span> e desejamos ajudar você a solucionar suas dúvidas. Com <span class="P-negrito">mais de 20 anos de experiência</span> e centenas de casos solucionados, atuamos em todo o território nacional e países do Mercosul. Nosso principal objetivo é esclarecer as dúvidas de nossos clientes, antes de tomar uma atitude diante a situação em que você está vivenciando, é importante que você tenha plena certeza de tudo que está acontecendo.
        </p>
        <p>
          Nossa agência é especializada em investigações de caráter conjugal, industrial, empresarial, comercial, familiar, política e assuntos privados. Seja qual for a complexidade dos desafios que você vêm enfrentando, a UNIVERSAL DETECTIVES terá a satisfação em ajuda-lo a desvendar o seu caso.
        </p>
        <div class="row mx-0">
          <ButtonScrollContato v-if="showScroll" name="Preencha nosso formulário" variation="lg-azul" />
          <a v-if="showQuatroSete" href="+554740549580" class="btn-azul-lg shadow mt-4 btn">
            +55 (47) 4054-9580
          </a>
          <a v-if="showQuatroOito" href="+554840528425" class="btn-azul-lg shadow mt-4 btn">
            +55 (48) 4052-8425
          </a>
          <a v-if="showQuatroNove" href="+554932400977" class="btn-azul-lg shadow mt-4 btn">
            +55 (49) 3240-0977
          </a>
          <a v-if="showQuatroUm" href="+554140639171" class="btn-azul-lg shadow mt-4 btn">
            +55 (41) 4063-9171
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ButtonScrollContato from '~/components/buttons/button-scroll-contato.vue'
import HeaderSections from '~/components/parts/HeaderSections.vue'

export default {
  components: { HeaderSections, ButtonScrollContato },
  // eslint-disable-next-line vue/require-prop-types
  props: {
    nameCidades: {
      type: String,
      default: ''
    },
    showScroll: {
      type: Boolean,
      default: false
    },
    showQuatroSete: {
      type: Boolean,
      default: false
    },
    showQuatroOito: {
      type: Boolean,
      default: false
    },
    showQuatroNove: {
      type: Boolean,
      default: false
    },
    showQuatroUm: {
      type: Boolean,
      default: false
    }
  }
}
</script>
<style lang="scss" scoped>
  .P-negrito {
    font-weight: 600;
  }
</style>
