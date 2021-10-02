<template>
  <div>
    <Cidades name-cidades="São João Batista - SC" :show-quatro-oito="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São João Batista - SC - Universal Detetives Particulares'
  }
}
</script>
