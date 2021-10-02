<template>
  <div>
    <Cidades name-cidades="Forquilhinha - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Forquilhinha - SC - Universal Detetives Particulares'
  }
}
</script>
