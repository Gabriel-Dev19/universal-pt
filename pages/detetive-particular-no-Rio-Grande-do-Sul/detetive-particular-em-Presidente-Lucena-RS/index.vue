<template>
  <div>
    <Cidades name-cidades="Presidente Lucena - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Presidente Lucena - RS - Universal Detetives Particulares'
  }
}
</script>
