<template>
  <div>
    <Cidades name-cidades="Rio de Janeiro - RJ" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Rio de Janeiro - RJ - Universal Detetives Particulares'
  }
}
</script>
