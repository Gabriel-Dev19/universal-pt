<template>
  <div>
    <Cidades name-cidades="Capão da Canoa - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Capão da Canoa - RS - Universal Detetives Particulares'
  }
}
</script>
