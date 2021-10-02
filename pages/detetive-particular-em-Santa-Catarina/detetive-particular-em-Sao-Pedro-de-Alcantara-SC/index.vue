<template>
  <div>
    <Cidades name-cidades="São Pedro de Alcântara - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Pedro de Alcântara - SC - Universal Detetives Particulares'
  }
}
</script>
