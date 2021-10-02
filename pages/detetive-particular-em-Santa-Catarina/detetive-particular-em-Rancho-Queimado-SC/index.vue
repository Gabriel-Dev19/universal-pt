<template>
  <div>
    <Cidades name-cidades="Rancho Queimado - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rancho Queimado - SC - Universal Detetives Particulares'
  }
}
</script>
