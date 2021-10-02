<template>
  <div>
    <Cidades name-cidades="Arroio do Meio - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Arroio do Meio - RS - Universal Detetives Particulares'
  }
}
</script>
