<template>
  <div>
    <Cidades name-cidades="Contenda - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Contenda - PR - Universal Detetives Particulares'
  }
}
</script>
