<template>
  <div>
    <Cidades name-cidades="Capitão - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Capitão - RS - Universal Detetives Particulares'
  }
}
</script>
