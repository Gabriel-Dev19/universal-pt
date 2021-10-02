<template>
  <div>
    <Cidades name-cidades="Nova Bréscia - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Nova Bréscia - RS - Universal Detetives Particulares'
  }
}
</script>
