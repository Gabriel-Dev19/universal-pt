<template>
  <div>
    <Cidades name-cidades="Balneário Gaivota - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Balneário Gaivota - SC - Universal Detetives Particulares'
  }
}
</script>
