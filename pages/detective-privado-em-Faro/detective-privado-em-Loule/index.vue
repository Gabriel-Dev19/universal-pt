<template>
  <div>
    <Cidades name-cidades="Loulé" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Loulé - Universal Detectives Privados'
  }
}
</script>
