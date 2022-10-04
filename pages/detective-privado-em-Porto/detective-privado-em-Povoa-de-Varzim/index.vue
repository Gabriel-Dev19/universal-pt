<template>
  <div>
    <Cidades name-cidades="Póvoa de Varzim" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Póvoa de Varzim - Universal Detectives Privados'
  }
}
</script>
