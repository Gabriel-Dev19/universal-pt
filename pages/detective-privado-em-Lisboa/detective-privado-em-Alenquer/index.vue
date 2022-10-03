<template>
  <div>
    <Cidades name-cidades="Alenquer" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Alenquer - Universal Detectives Privados'
  }
}
</script>
