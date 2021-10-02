<template>
  <div>
    <Cidades name-cidades="Capela de Santana - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Capela de Santana - RS - Universal Detetives Particulares'
  }
}
</script>
