<template>
  <div>
    <Cidades name-cidades="Santa Maria da Feira" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Santa Maria da Feira - Universal Detectives Privados'
  }
}
</script>
