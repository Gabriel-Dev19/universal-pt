<template>
  <div>
    <Cidades name-cidades="Camaquã - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Camaquã - RS - Universal Detetives Particulares'
  }
}
</script>
