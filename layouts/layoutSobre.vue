<template>
  <div>
    <NavbarMobile />
    <NavbarDesktop />
    <Home
      name-btn="Nossos serviços"
      hash-btn="servicos"
      title-principal="Sobre a universal detetives"
      description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi iste deleniti
        dolore quos dicta illum in consectetur aspernatur voluptates culpa amet tempore, repellat
        quae eos odio vel. Assumenda!"
    />
    <Nuxt />
    <SwiperVertical style="margin-top: 150px;" />
    <Servicos />
    <Solutions />
    <Questions />
    <Faq />
    <Contato />
    <Footer />
  </div>
</template>

<script>
import Vue from 'vue'
import VueSmoothScroll from '../node_modules/vue2-smooth-scroll'
Vue.use(VueSmoothScroll)
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

}
</script>
