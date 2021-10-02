<template>
  <div>
    <Cidades name-cidades="Três Cachoeiras - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Três Cachoeiras - RS - Universal Detetives Particulares'
  }
}
</script>
