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
    <btnWhatsappFlutuante />
    <client-only>
      <Cookie />
    </client-only>
  </div>
</template>

<script>
import Vue from 'vue'
import VueScrollTo from '../node_modules/vue-scrollto'
import btnWhatsappFlutuante from '~/components/buttons/btn-whatsapp-flutuante.vue'
import Cookie from '~/components/Cookie.vue'
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
  components: { btnWhatsappFlutuante, Cookie }
}
</script>
