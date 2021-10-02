<template>
  <div>
    <Cidades name-cidades="Vespasiano Correia - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Vespasiano Correia - RS - Universal Detetives Particulares'
  }
}
</script>
