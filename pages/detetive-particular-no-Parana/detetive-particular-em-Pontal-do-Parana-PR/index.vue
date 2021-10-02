<template>
  <div>
    <Cidades name-cidades="Pontal do Paraná - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Pontal do Paraná - PR - Universal Detetives Particulares'
  }
}
</script>
