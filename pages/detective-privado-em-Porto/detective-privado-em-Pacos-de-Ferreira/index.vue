<template>
  <div>
    <Cidades name-cidades="Paços de Ferreira" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Paços de Ferreira - Universal Detectives Privados'
  }
}
</script>
