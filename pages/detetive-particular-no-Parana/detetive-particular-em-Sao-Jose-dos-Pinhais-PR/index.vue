<template>
  <div>
    <Cidades name-cidades="São José dos Pinhais - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São José dos Pinhais - PR - Universal Detetives Particulares'
  }
}
</script>
