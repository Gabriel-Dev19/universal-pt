<template>
  <div>
    <Cidades name-cidades="Odivelas" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Odivelas - Universal Detectives Privados'
  }
}
</script>
