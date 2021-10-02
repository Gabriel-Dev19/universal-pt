<template>
  <div>
    <Cidades name-cidades="Santo Antônio da Patrulha - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Santo Antônio da Patrulha - RS - Universal Detetives Particulares'
  }
}
</script>
