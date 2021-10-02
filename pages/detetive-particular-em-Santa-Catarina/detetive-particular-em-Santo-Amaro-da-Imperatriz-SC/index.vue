<template>
  <div>
    <Cidades name-cidades="Santo Amaro da Imperatriz - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santo Amaro da Imperatriz - SC - Universal Detetives Particulares'
  }
}
</script>
