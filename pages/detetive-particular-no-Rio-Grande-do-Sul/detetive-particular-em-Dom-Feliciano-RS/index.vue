<template>
  <div>
    <Cidades name-cidades="Dom Feliciano - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Dom Feliciano - RS - Universal Detetives Particulares'
  }
}
</script>
