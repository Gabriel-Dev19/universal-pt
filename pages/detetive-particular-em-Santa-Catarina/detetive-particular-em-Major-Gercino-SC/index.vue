<template>
  <div>
    <Cidades name-cidades="Major Gercino - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Major Gercino - SC - Universal Detetives Particulares'
  }
}
</script>
