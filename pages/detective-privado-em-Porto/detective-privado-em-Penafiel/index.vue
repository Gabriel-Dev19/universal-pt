<template>
  <div>
    <Cidades name-cidades="Penafiel" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Penafiel - Universal Detectives Privados'
  }
}
</script>
