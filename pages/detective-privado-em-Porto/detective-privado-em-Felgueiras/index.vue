<template>
  <div>
    <Cidades name-cidades="Felgueiras" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Felgueiras - Universal Detectives Privados'
  }
}
</script>
