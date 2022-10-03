<template>
  <div>
    <Cidades name-cidades="Montijo" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Montijo - Universal Detectives Privados'
  }
}
</script>
