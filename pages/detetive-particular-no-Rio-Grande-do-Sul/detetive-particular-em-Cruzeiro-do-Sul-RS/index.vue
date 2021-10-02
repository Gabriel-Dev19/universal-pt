<template>
  <div>
    <Cidades name-cidades="Cruzeiro do Sul - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Cruzeiro do Sul - RS - Universal Detetives Particulares'
  }
}
</script>
