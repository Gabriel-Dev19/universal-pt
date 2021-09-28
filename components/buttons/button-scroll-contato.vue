<template lang="">
  <div>
    <button v-if="variation === 'seta'" class="link-seta pl-0 text-left pt-0 pb-0 btn cursor-pointer" @click="ScrollContato">
      {{ name }}
      <div class="mae_seta">
        <div class="seta">
          <ion-icon name="chevron-forward-outline" />
        </div>
      </div>
    </button>
    <button v-if="variation === 'lg-azul'" class="btn-azul-lg shadow mt-4 btn" @click="ScrollContato">
      {{ name }}
    </button>
  </div>
</template>
<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['name', 'variation'],
  data () {
    return {
      Quantidade_retira_hash: 0
    }
  },
  methods: {
    ScrollContato () {
      this.$smoothScroll({
        scrollTo: document.getElementById('contato'),
        duration: 500,
        offset: -190
      })
      setTimeout(() => {
        this.HideHash()
      }, 490)
    },
    HideHash () {
      this.Quantidade_retira_hash = 0
      const interval = setInterval(() => {
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
        this.Quantidade_retira_hash++
        if (this.Quantidade_retira_hash > 5) { clearInterval(interval) }
      }, 0)
    }
  }
}
</script>
<style lang="">

</style>
