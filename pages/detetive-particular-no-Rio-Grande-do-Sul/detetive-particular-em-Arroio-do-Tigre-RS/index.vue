<template>
  <div>
    <Cidades name-cidades="Arroio do Tigre - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Arroio do Tigre - RS - Universal Detetives Particulares'
  }
}
</script>
