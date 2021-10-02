<template>
  <div>
    <Cidades name-cidades="Chapecó - SC" :show-quatro-nove="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Chapecó - SC - Universal Detetives Particulares'
  }
}
</script>
