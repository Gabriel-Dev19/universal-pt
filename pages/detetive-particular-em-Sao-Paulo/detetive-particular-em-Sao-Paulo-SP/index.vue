<template>
  <div>
    <Cidades name-cidades="São Paulo - SP" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em São Paulo - SP - Universal Detetives Particulares'
  }
}
</script>
