<template>
  <div>
    <Cidades name-cidades="São Leopoldo - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Leopoldo - RS - Universal Detetives Particulares'
  }
}
</script>
