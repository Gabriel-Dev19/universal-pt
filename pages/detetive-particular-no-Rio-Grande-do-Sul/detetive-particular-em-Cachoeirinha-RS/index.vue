<template>
  <div>
    <Cidades name-cidades="Cachoeirinha - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Cachoeirinha - RS - Universal Detetives Particulares'
  }
}
</script>
