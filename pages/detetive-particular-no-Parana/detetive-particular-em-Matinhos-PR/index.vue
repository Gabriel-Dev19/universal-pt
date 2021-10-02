<template>
  <div>
    <Cidades name-cidades="Matinhos - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Matinhos - PR - Universal Detetives Particulares'
  }
}
</script>
