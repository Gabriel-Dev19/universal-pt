<template>
  <section>
    <div class="page-404">
      <NavbarMobile />
      <NavbarDesktop />
      <Home
        name-btn=""
        title-principal="404: erro ao requisitar a página :( tente novamente!"
        description=""
      />
    </div>
    <Contato />
    <Footer />
    <btnWhatsappFlutuante />
  </section>
</template>

<script>
import Vue from 'vue'
import VueScrollTo from '../node_modules/vue-scrollto'
import btnWhatsappFlutuante from '~/components/buttons/btn-whatsapp-flutuante.vue'
Vue.use(VueScrollTo)
Vue.directive('scroll', {
  inserted (el, binding) {
    const f = function (evt) {
      if (binding.value(evt, el)) {
        window.removeEventListener('scroll', f)
      }
    }
    window.addEventListener('scroll', f)
  }
})
export default {
  components: { btnWhatsappFlutuante },
  layout: 'error',
  // eslint-disable-next-line vue/require-prop-types
  props: ['error']
}
</script>

<style lang="scss" scoped>
  .page-404{
    background: url(../assets/img/bg-universe.webp) center center no-repeat;
    background-size: cover;
    min-height: 100vh;
  }
</style>
