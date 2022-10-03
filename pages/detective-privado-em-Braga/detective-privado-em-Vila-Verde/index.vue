<template>
  <div>
    <Cidades name-cidades="Vila Verde" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Vila Verde - Universal Detectives Privados'
  }
}
</script>
