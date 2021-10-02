<template>
  <div>
    <Cidades name-cidades="Pouso Redondo - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Pouso Redondo - SC - Universal Detetives Particulares'
  }
}
</script>
