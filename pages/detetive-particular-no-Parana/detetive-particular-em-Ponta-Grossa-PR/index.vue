<template>
  <div>
    <Cidades name-cidades="Ponta Grossa - PR" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Ponta Grossa - PR - Universal Detetives Particulares'
  }
}
</script>
