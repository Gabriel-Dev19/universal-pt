<template>
  <div>
    <Cidades name-cidades="Roca Sales - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Roca Sales - RS - Universal Detetives Particulares'
  }
}
</script>
