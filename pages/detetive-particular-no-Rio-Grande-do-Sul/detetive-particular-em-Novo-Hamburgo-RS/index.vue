<template>
  <div>
    <Cidades name-cidades="Novo Hamburgo - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Novo Hamburgo - RS - Universal Detetives Particulares'
  }
}
</script>
