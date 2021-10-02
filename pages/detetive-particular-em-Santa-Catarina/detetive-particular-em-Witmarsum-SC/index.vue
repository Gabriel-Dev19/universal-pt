<template>
  <div>
    <Cidades name-cidades="Witmarsum - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Witmarsum - SC - Universal Detetives Particulares'
  }
}
</script>
