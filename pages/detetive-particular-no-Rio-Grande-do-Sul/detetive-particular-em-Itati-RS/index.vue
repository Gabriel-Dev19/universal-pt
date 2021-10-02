<template>
  <div>
    <Cidades name-cidades="Itati - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Itati - RS - Universal Detetives Particulares'
  }
}
</script>
