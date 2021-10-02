<template>
  <div>
    <Cidades name-cidades="Antonina - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Antonina - PR - Universal Detetives Particulares'
  }
}
</script>
