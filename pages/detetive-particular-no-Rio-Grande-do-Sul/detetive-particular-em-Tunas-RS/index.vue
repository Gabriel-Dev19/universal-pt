<template>
  <div>
    <Cidades name-cidades="Tunas do Paraná - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Tunas do Paraná - RS - Universal Detetives Particulares'
  }
}
</script>
