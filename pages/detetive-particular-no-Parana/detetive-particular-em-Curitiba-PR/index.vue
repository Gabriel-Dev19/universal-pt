<template>
  <div>
    <Cidades name-cidades="Curitiba - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Curitiba - PR - Universal Detetives Particulares'
  }
}
</script>
