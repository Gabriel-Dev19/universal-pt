<template>
  <div>
    <Cidades name-cidades="Guanamirim - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Guanamirim - SC - Universal Detetives Particulares'
  }
}
</script>
