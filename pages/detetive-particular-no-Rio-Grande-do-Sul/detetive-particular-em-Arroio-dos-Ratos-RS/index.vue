<template>
  <div>
    <Cidades name-cidades="Arroio dos Ratos - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Arroio dos Ratos - RS - Universal Detetives Particulares'
  }
}
</script>
