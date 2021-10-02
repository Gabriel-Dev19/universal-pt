<template>
  <div>
    <Cidades name-cidades="Chuvisca - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Chuvisca - RS - Universal Detetives Particulares'
  }
}
</script>
