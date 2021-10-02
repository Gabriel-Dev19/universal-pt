<template>
  <div>
    <Cidades name-cidades="Bom Princípio - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Bom Princípio - RS - Universal Detetives Particulares'
  }
}
</script>
