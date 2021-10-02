<template>
  <div>
    <Cidades name-cidades="Brusque - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Brusque - SC - Universal Detetives Particulares'
  }
}
</script>
