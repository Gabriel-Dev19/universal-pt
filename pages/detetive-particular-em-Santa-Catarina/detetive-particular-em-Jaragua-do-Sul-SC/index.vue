<template>
  <div>
    <Cidades name-cidades="Jaraguá do Sul - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Jaraguá do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
