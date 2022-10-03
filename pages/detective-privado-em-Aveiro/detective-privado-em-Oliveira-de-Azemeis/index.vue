<template>
  <div>
    <Cidades name-cidades="Oliveira de Azeméis" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Oliveira de Azeméis - Universal Detectives Privados'
  }
}
</script>
