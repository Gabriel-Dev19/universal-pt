<template>
  <div>
    <Cidades name-cidades="Nova Santa Rita - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Nova Santa Rita - RS - Universal Detetives Particulares'
  }
}
</script>
