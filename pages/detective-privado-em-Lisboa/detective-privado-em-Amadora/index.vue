<template>
  <div>
    <Cidades name-cidades="Amadora" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Amadora - Universal Detectives Privados'
  }
}
</script>
