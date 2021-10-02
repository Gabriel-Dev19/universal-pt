<template>
  <div>
    <Cidades name-cidades="Dom Pedro de Alcântara - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Dom Pedro de Alcântara - RS - Universal Detetives Particulares'
  }
}
</script>
