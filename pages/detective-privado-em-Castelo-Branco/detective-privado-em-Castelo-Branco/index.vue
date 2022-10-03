<template>
  <div>
    <Cidades name-cidades="Castelo Branco" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Castelo Branco - Universal Detectives Privados'
  }
}
</script>
