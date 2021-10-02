<template>
  <div>
    <Cidades name-cidades="Capivari de Baixo - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Capivari de Baixo - SC - Universal Detetives Particulares'
  }
}
</script>
