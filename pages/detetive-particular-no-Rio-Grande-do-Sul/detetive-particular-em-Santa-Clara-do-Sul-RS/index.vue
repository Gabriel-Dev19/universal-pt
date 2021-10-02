<template>
  <div>
    <Cidades name-cidades="Santa Clara do Sul - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santa Clara do Sul - RS - Universal Detetives Particulares'
  }
}
</script>
