<template>
  <div>
    <Cidades name-cidades="Montenegro - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Montenegro - RS - Universal Detetives Particulares'
  }
}
</script>
