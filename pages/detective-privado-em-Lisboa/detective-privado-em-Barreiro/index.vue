<template>
  <div>
    <Cidades name-cidades="Barreiro" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Barreiro - Universal Detectives Privados'
  }
}
</script>
