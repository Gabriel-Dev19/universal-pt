<template>
  <div>
    <Cidades name-cidades="Viana do Castelo" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Viana do Castelo - Universal Detectives Privados'
  }
}
</script>
