<template>
  <div>
    <Cidades name-cidades="Balneário Piçarras - SC" :show-quatro-nove="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Balneário Piçarras - SC - Universal Detetives Particulares'
  }
}
</script>
