<template>
  <div>
    <Cidades name-cidades="Vale do Sol - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Vale do Sol - RS - Universal Detetives Particulares'
  }
}
</script>
