<template>
  <div>
    <Cidades name-cidades="Santana do livramento - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santana do livramento - RS - Universal Detetives Particulares'
  }
}
</script>
