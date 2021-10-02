<template>
  <div>
    <Cidades name-cidades="Braço do Trombudo - SC" :show-quatro-sete="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Braço do Trombudo - SC - Universal Detetives Particulares'
  }
}
</script>
