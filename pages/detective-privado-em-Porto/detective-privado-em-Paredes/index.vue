<template>
  <div>
    <Cidades name-cidades="Paredes" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Paredes - Universal Detectives Privados'
  }
}
</script>
