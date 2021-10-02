<template>
  <div>
    <Cidades name-cidades="Luís Alves - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Luís Alves - SC - Universal Detetives Particulares'
  }
}
</script>
