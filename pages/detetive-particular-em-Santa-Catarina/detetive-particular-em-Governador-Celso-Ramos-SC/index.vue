<template>
  <div>
    <Cidades name-cidades="Governador Celso Ramos - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Governador Celso Ramos - SC - Universal Detetives Particulares'
  }
}
</script>
