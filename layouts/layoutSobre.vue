<template>
  <div>
    <NavbarMobile />
    <NavbarDesktop />
    <Nuxt />
    <SwiperVertical style="margin-top: 150px;" />
    <Servicos />
    <Solutions />
    <Questions />
    <Faq />
    <Contato />
    <Footer />
    <btn-whatsapp-flutuante />
  </div>
</template>

<script>
import Vue from 'vue'
import VueScrollTo from '../node_modules/vue-scrollto'
import BtnWhatsappFlutuante from '~/components/buttons/btn-whatsapp-flutuante.vue'
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
  components: { BtnWhatsappFlutuante }
}
</script>
