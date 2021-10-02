<template>
  <div>
    <Cidades name-cidades="Rio do Campo - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rio do Campo - SC - Universal Detetives Particulares'
  }
}
</script>
