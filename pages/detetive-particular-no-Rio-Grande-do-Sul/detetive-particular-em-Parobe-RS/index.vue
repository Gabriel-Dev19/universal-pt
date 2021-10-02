<template>
  <div>
    <Cidades name-cidades="Parobé - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Parobé - RS - Universal Detetives Particulares'
  }
}
</script>
