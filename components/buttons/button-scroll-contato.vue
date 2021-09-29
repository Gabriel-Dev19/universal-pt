<template lang="">
  <div>
    <button v-if="variation === 'seta'" v-scroll-to="optionsScroll" class="link-seta pl-0 text-left pt-0 pb-0 btn cursor-pointer">
      {{ name }}
      <div class="mae_seta">
        <div class="seta">
          <ion-icon name="chevron-forward-outline" />
        </div>
      </div>
    </button>
    <button v-if="variation === 'lg-azul'" v-scroll-to="optionsScroll" class="btn-azul-lg shadow mt-4 btn">
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
      Quantidade_retira_hash: 0,
      optionsScroll: {
        el: '#contato',
        offset: -190
      }
    }
  }
}
</script>
<style lang="">

</style>
