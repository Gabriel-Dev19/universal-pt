<template>
  <div>
    <Cidades name-cidades="Amaral Ferrador - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Amaral Ferrador - RS - Universal Detetives Particulares'
  }
}
</script>
