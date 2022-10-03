<template>
  <div>
    <Cidades name-cidades="Barcelos" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Barcelos - Universal Detectives Privados'
  }
}
</script>
