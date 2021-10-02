<template>
  <div>
    <Cidades name-cidades="Vidal Ramos - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Vidal Ramos - SC - Universal Detetives Particulares'
  }
}
</script>
