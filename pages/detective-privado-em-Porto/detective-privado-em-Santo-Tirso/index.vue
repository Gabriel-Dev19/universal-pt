<template>
  <div>
    <Cidades name-cidades="Santo Tirso" :show-scroll="true" />
  </div>
</template>

<script>
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detective privado em Santo Tirso - Universal Detectives Privados'
  }
}
</script>
