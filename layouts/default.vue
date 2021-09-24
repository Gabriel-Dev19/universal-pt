<template>
  <div>
    <NavbarMobile />
    <NavbarDesktop />
    <Nuxt />
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
