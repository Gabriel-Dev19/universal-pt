<template>
  <div>
    <Cidades name-cidades="Belo Horizonte - MG" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Belo Horizonte - MG - Universal Detetives Particulares'
  }
}
</script>
