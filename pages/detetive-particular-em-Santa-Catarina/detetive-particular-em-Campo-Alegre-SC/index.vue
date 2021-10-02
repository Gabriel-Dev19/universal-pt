<template>
  <div>
    <Cidades name-cidades="Campo Alegre - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Campo Alegre - SC - Universal Detetives Particulares'
  }
}
</script>
