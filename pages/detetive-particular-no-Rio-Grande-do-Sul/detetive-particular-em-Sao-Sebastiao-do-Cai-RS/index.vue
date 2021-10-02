<template>
  <div>
    <Cidades name-cidades="São Sebastião do Cai - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Sebastião do Cai - RS - Universal Detetives Particulares'
  }
}
</script>
