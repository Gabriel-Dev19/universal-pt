<template>
  <div>
    <Cidades name-cidades="Butiá - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Butiá - RS - Universal Detetives Particulares'
  }
}
</script>
