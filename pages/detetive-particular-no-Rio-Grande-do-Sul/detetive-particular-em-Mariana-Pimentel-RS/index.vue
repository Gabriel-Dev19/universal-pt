<template>
  <div>
    <Cidades name-cidades="Mariana Pimentel - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Mariana Pimentel - RS - Universal Detetives Particulares'
  }
}
</script>
