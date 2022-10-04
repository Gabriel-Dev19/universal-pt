<template>
  <div>
    <Cidades name-cidades="Marco de Canaveses" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Marco de Canaveses - Universal Detectives Privados'
  }
}
</script>
