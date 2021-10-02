<template>
  <div>
    <Cidades name-cidades="Presidente Getúlio - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Presidente Getúlio - SC - Universal Detetives Particulares'
  }
}
</script>
