<template>
  <div>
    <Cidades name-cidades="Maringá - PR" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Maringá - PR - Universal Detetives Particulares'
  }
}
</script>
