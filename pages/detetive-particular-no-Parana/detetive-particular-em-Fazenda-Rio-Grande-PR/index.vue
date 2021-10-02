<template>
  <div>
    <Cidades name-cidades="Fazenda Rio Grande - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Fazenda Rio Grande - PR - Universal Detetives Particulares'
  }
}
</script>
