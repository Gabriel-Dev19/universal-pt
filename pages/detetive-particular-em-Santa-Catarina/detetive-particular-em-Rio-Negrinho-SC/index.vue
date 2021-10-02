<template>
  <div>
    <Cidades name-cidades="Rio Negrinho - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rio Negrinho - SC - Universal Detetives Particulares'
  }
}
</script>
