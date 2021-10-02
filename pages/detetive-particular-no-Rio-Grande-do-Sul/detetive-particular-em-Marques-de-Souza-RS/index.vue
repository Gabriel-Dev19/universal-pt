<template>
  <div>
    <Cidades name-cidades="Marques de Souza - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Marques de Souza - RS - Universal Detetives Particulares'
  }
}
</script>
