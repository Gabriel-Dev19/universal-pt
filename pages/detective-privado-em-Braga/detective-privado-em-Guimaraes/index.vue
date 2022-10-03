<template>
  <div>
    <Cidades name-cidades="Guimarães" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Guimarães - Universal Detectives Privados'
  }
}
</script>
