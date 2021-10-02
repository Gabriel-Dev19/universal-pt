<template>
  <div>
    <Cidades name-cidades="Turvo - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Turvo - SC - Universal Detetives Particulares'
  }
}
</script>
