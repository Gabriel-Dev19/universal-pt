<template>
  <div>
    <Cidades name-cidades="Agrolândia - SC" :show-quatro-um="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Agrolândia - SC - Universal Detetives Particulares'
  }
}
</script>
