<template>
  <div>
    <Cidades name-cidades="Doutor Ulysses - PR" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Doutor Ulysses - PR - Universal Detetives Particulares'
  }
}
</script>
