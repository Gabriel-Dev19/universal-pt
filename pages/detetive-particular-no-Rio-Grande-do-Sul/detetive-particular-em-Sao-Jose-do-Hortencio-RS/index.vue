<template>
  <div>
    <Cidades name-cidades="São José do Hortêncio - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São José do Hortêncio - RS - Universal Detetives Particulares'
  }
}
</script>
