<template>
  <div>
    <Cidades name-cidades="Cerro Branco - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Cerro Branco - RS - Universal Detetives Particulares'
  }
}
</script>
