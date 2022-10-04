<template>
  <div>
    <Cidades name-cidades="Vila Nova de Gaia" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Vila Nova de Gaia - Universal Detectives Privados'
  }
}
</script>
