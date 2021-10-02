<template>
  <div>
    <Cidades name-cidades="Passo do Sobrado - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Passo do Sobrado - RS - Universal Detetives Particulares'
  }
}
</script>
