<template>
  <div>
    <Home title-home="Detetive particular em Feliz - RS" :bg-home="true" />
    <Cidades name-cidades="Feliz - RS" :show-scroll="true" />
  </div>
</template>

<script>
import Home from '~/components/Home.vue'
import Cidades from '~/components/parts/Cidades.vue'
export default {
  components: { Home, Cidades },
  layout: 'layoutSobre',
  head: {
    title: 'Detetive particular em Feliz - RS - Agência de detetives Graziella Bastos'
  },
  methods: {
    HideHash () {
      let scrollV; let scrollH; const loc = window.location
      if ('replaceState' in history) {
        history.replaceState('', document.title, loc.pathname + loc.search)
      } else {
        // Prevent scrolling by storing the page's current scroll offset
        scrollV = document.body.scrollTop
        scrollH = document.body.scrollLeft
        loc.hash = ''
        // Restore the scroll offset, should be flicker free
        document.body.scrollTop = scrollV
        document.body.scrollLeft = scrollH
      }
    }
  }
}
</script>
