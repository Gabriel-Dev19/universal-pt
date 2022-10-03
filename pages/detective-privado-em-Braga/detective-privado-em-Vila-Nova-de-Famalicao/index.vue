<template>
  <div>
    <Cidades name-cidades="Vila Nova de Famalicão" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Vila Nova de Famalicão - Universal Detectives Privados'
  }
}
</script>
