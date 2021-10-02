<template>
  <div>
    <Cidades name-cidades="São Joaquim - SC" :show-quatro-nove="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Joaquim - SC - Universal Detetives Particulares'
  }
}
</script>
