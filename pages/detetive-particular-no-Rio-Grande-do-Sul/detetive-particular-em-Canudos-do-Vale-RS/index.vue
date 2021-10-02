<template>
  <div>
    <Cidades name-cidades="Canudos do Vale - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Canudos do Vale - RS - Universal Detetives Particulares'
  }
}
</script>
