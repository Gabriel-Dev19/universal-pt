<template>
  <div>
    <Cidades name-cidades="Torres Vedras" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Torres Vedras - Universal Detectives Privados'
  }
}
</script>
