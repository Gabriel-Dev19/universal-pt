<template>
  <div>
    <Cidades name-cidades="Salvador do Sul - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Salvador do Sul - RS - Universal Detetives Particulares'
  }
}
</script>
