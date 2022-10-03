<template>
  <div>
    <Cidades name-cidades="Sesimbra" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Sesimbra - Universal Detectives Privados'
  }
}
</script>
