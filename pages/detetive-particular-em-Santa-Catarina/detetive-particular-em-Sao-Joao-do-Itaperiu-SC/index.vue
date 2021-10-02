<template>
  <div>
    <Cidades name-cidades="São João do Itaperiú - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São João do Itaperiú - SC - Universal Detetives Particulares'
  }
}
</script>
