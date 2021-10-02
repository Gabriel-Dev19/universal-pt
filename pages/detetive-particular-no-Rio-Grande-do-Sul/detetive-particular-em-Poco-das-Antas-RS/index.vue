<template>
  <div>
    <Cidades name-cidades="Poço das Antas - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Poço das Antas - RS - Universal Detetives Particulares'
  }
}
</script>
