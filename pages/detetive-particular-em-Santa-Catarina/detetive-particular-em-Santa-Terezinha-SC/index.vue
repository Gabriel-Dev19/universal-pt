<template>
  <div>
    <Cidades name-cidades="Santa Terezinha - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santa Terezinha - SC - Universal Detetives Particulares'
  }
}
</script>
