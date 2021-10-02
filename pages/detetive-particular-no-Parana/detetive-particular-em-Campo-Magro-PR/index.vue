<template>
  <div>
    <Cidades name-cidades="Campo Magro - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Campo Magro - PR - Universal Detetives Particulares'
  }
}
</script>
