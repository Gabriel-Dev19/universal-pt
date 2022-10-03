<template>
  <div>
    <Cidades name-cidades="Portimão" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Portimão - Universal Detectives Privados'
  }
}
</script>
