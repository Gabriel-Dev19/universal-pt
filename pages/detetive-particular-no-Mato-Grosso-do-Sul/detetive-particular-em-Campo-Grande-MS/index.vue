<template>
  <div>
    <Cidades name-cidades="Campo Grande - MS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Campo Grande - MS - Universal Detetives Particulares'
  }
}
</script>
