<template>
  <div>
    <Cidades name-cidades="Nova Hartz - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Nova Hartz - RS - Universal Detetives Particulares'
  }
}
</script>
