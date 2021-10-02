<template>
  <div>
    <Cidades name-cidades="Osório - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Osório - RS - Universal Detetives Particulares'
  }
}
</script>
