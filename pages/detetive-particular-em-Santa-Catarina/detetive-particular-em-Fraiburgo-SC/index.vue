<template>
  <div>
    <Cidades name-cidades="Fraiburgo - SC" :show-quatro-nove="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Fraiburgo - SC - Universal Detetives Particulares'
  }
}
</script>
