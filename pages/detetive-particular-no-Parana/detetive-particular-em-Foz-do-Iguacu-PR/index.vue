<template>
  <div>
    <Cidades name-cidades="Foz do Iguaçú - PR" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Foz do Iguaçú - PR - Universal Detetives Particulares'
  }
}
</script>
