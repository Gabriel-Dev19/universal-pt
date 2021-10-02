<template>
  <div>
    <Cidades name-cidades="Palhoça - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Palhoça - SC - Universal Detetives Particulares'
  }
}
</script>
