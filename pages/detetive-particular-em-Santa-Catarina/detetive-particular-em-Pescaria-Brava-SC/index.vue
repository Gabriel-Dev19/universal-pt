<template>
  <div>
    <Cidades name-cidades="Pescaria Brava - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Pescaria Brava - SC - Universal Detetives Particulares'
  }
}
</script>
