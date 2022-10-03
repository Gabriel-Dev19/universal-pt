<template>
  <div>
    <Cidades name-cidades="Oeiras" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Oeiras - Universal Detectives Privados'
  }
}
</script>
