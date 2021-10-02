<template>
  <div>
    <Cidades name-cidades="Londrina - PR" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Londrina - PR - Universal Detetives Particulares'
  }
}
</script>
