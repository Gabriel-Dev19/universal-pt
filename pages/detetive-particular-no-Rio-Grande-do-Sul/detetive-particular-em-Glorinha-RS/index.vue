<template>
  <div>
    <Cidades name-cidades="Glorinha - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Glorinha - RS - Universal Detetives Particulares'
  }
}
</script>
