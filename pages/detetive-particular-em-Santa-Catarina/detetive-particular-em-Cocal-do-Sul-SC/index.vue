<template>
  <div>
    <Cidades name-cidades="Cocal do Sul - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Cocal do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
