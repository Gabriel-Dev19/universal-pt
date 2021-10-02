<template>
  <div>
    <Cidades name-cidades="Goiânia - GO" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Goiânia - GO - Universal Detetives Particulares'
  }
}
</script>
