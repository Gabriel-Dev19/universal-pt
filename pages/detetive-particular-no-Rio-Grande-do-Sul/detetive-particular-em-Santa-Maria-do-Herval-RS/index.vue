<template>
  <div>
    <Cidades name-cidades="Santa Maria do Herval - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santa Maria do Herval - RS - Universal Detetives Particulares'
  }
}
</script>
