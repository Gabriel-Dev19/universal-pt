<template>
  <div>
    <Cidades name-cidades="Minas do Leão - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Minas do Leão - RS - Universal Detetives Particulares'
  }
}
</script>
