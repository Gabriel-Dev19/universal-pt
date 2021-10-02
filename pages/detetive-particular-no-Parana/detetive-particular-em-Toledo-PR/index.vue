<template>
  <div>
    <Cidades name-cidades="Toledo - PR" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Toledo - PR - Universal Detetives Particulares'
  }
}
</script>
