<template>
  <div>
    <Cidades name-cidades="Palmela" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Palmela - Universal Detectives Privados'
  }
}
</script>
