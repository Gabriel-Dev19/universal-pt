<template>
  <div>
    <Cidades name-cidades="General Câmara - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em General Câmara - RS - Universal Detetives Particulares'
  }
}
</script>
