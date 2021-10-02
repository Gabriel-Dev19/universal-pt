<template>
  <div>
    <Cidades name-cidades="Brasília - DF" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Brasília - DF - Universal Detetives Particulares'
  }
}
</script>
