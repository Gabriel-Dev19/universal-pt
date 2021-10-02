<template>
  <div>
    <Cidades name-cidades="Lapa - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Lapa - PR - Universal Detetives Particulares'
  }
}
</script>
