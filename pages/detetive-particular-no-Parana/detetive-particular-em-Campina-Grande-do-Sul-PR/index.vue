<template>
  <div>
    <Cidades name-cidades="Campina Grande do Sul - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Campina Grande do Sul - PR - Universal Detetives Particulares'
  }
}
</script>
