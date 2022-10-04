<template>
  <div>
    <Cidades name-cidades="Viseu" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Viseu - Universal Detectives Privados'
  }
}
</script>
