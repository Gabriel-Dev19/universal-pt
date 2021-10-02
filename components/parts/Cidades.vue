<template>
  <div>
    <Home
      name-btn="Saiba mais"
      hash-btn="sobre"
      :title-principal="`Detetive particular em ${nameCidades}`"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../assets/img/detetive-lupa.webp')"
        title-badge="sobre nós"
        parte-azul="Encontre detetives:"
        :title-header="nameCidades"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum omnis
        aliquid perspiciatis quos, sequi ratione sunt possimus corrupti velit porro? Nobis
        ipsa dicta quasi repellendus, ducimus et deleniti tenetur delectus?"
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          Algum tema?
        </h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
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

</style>
