<template>
  <div>
    <Cidades name-cidades="Figueira da Foz" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Figueira da Foz - Universal Detectives Privados'
  }
}
</script>
