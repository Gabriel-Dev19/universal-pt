<template>
  <div>
    <Cidades name-cidades="Rio Branco do Sul - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rio Branco do Sul - PR - Universal Detetives Particulares'
  }
}
</script>
