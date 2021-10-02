<template>
  <div>
    <Cidades name-cidades="Timbé do Sul - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Timbé do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
