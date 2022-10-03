<template>
  <div>
    <Cidades name-cidades="Pombal" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Pombal - Universal Detectives Privados'
  }
}
</script>
