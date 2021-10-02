<template>
  <div>
    <Cidades name-cidades="Santa Rosa de Lima - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santa Rosa de Lima - SC - Universal Detetives Particulares'
  }
}
</script>
