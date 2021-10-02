<template>
  <div>
    <Cidades name-cidades="Chapadão do Lageado - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Chapadão do Lageado - SC - Universal Detetives Particulares'
  }
}
</script>
