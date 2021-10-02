<template>
  <div>
    <Cidades name-cidades="Braço do Norte - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Braço do Norte - SC - Universal Detetives Particulares'
  }
}
</script>
