<template>
  <div>
    <Cidades name-cidades="Mirim Doce - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Mirim Doce - SC - Universal Detetives Particulares'
  }
}
</script>
