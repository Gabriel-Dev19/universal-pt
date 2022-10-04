<template>
  <div>
    <Cidades name-cidades="Seixal" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Seixal - Universal Detectives Privados'
  }
}
</script>
