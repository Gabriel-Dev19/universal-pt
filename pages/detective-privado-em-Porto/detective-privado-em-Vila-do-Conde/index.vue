<template>
  <div>
    <Cidades name-cidades="Vila do Conde" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Vila do Conde - Universal Detectives Privados'
  }
}
</script>
