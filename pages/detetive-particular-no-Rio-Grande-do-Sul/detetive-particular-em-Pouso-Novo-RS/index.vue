<template>
  <div>
    <Cidades name-cidades="Pouso Novo - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Pouso Novo - RS - Universal Detetives Particulares'
  }
}
</script>
