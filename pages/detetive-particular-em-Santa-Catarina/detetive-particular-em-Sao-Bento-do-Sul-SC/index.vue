<template>
  <div>
    <Cidades name-cidades="São Bento do Sul - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Bento do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
