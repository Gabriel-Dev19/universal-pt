<template>
  <div>
    <Cidades name-cidades="Rio do Sul - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rio do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
