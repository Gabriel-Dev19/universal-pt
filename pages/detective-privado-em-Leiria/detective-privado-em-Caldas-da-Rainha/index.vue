<template>
  <div>
    <Cidades name-cidades="Caldas da Rainha" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Caldas da Rainha - Universal Detectives Privados'
  }
}
</script>
