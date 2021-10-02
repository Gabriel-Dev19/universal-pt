<template>
  <div>
    <Cidades name-cidades="Balneário Arroio do Silva - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Balneário Arroio do Silva - SC - Universal Detetives Particulares'
  }
}
</script>
