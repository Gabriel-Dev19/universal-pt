<template>
  <div>
    <Cidades name-cidades="Morro Reuter - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Morro Reuter - RS - Universal Detetives Particulares'
  }
}
</script>
