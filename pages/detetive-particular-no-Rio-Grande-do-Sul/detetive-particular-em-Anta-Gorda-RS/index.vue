<template>
  <div>
    <Cidades name-cidades="Anta Gorda - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Anta Gorda - RS - Universal Detetives Particulares'
  }
}
</script>
