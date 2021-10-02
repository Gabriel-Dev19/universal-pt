<template>
  <div>
    <Cidades name-cidades="Fazenda Vilanova - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Fazenda Vilanova - RS - Universal Detetives Particulares'
  }
}
</script>
