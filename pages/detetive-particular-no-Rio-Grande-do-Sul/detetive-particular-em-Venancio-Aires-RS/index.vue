<template>
  <div>
    <Cidades name-cidades="Venâncio Aires - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Venâncio Aires - RS - Universal Detetives Particulares'
  }
}
</script>
