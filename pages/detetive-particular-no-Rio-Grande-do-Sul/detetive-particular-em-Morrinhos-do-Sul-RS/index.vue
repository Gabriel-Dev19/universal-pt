<template>
  <div>
    <Cidades name-cidades="Morrinhos do Sul - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Morrinhos do Sul - RS - Universal Detetives Particulares'
  }
}
</script>
