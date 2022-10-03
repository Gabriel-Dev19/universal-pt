<template>
  <div>
    <Cidades name-cidades="Almada" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Almada - Universal Detectives Privados'
  }
}
</script>
