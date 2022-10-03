<template>
  <div>
    <Cidades name-cidades="Vila Franca de Xira" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Vila Franca de Xira - Universal Detectives Privados'
  }
}
</script>
