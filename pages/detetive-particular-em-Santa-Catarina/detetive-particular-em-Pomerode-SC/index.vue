<template>
  <div>
    <Cidades name-cidades="Pomerode - SC" :show-quatro-nove="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Pomerode - SC - Universal Detetives Particulares'
  }
}
</script>
