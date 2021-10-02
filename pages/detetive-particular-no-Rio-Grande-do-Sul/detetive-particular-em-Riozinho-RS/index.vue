<template>
  <div>
    <Cidades name-cidades="Riozinho - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Riozinho - RS - Universal Detetives Particulares'
  }
}
</script>
