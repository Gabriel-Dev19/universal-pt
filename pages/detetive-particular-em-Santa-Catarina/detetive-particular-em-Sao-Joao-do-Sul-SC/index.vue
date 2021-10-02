<template>
  <div>
    <Cidades name-cidades="São João do Sul - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São João do Sul - SC - Universal Detetives Particulares'
  }
}
</script>
