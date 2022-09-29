<template>
  <transition enter-active-class="animate__animated animate__fadeIn" leave-active-class="animate__animated animate__fadeOut">
    <div v-if="isOpen" class="cookie mb-2 mb-sm-4 px-0 col-12">
      <div class="ml-2 ml-sm-4 bg-white div-cookie py-3 shadow-lg px-0">
        <div class="d-flex px-3 align-items-center">
          <div class="align-items-center row mx-auto col-12 px-0">
            <p class="col px-0 text-xs-center text-sm-center text-xl-left mb-0 fs-15">
              <ion-icon class="fs-25" name="alert-circle-outline" style="margin-bottom: -2px;" />
              Usamos cookies para fornecer nossos serviços e para análises e marketing. Para saber mais sobre nosso uso
              de cookies, consulte nossa <button class="btn fs-15 text-underline py-0 px-0" @click="Politica">
                Política de Privacidade
              </button>.
            </p>
            <div class="d-flex align-items-center col-12 px-0 row mx-auto">
              <button class="btn border-radius-0 fw-500 px-15 mt-3 btn-dark mr-2" @click="accept">
                {{ buttonTextAccept }}
              </button>
              <button class="btn border-radius-0 px-15 fw-500 mt-3 btn-outline-dark" text @click="deny">
                {{ buttonTextDeny }}
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'CookieMessage',
  props: {
    buttonTextAccept: {
      type: String,
      default: 'Aceitar Cookies'
    },
    buttonTextDeny: {
      type: String,
      default: 'Negar'
    },
    message: {
      type: String,
      default:
        'We use cookies to provide our services and for analytics and marketing. To find out more about our use of cookies, please see our Privacy Policy. By continuing to browse our website, you agree to our use of cookies.'
    },
    position: {
      type: String,
      default: 'top'
    }
  },
  data () {
    return {
      isOpen: false
    }
  },
  computed: {
    containerPosition () {
      return `cookie--${this.position}`
    }
  },
  created () {
    if (!this.getGDPR() === true) {
      this.isOpen = true
    }
  },
  methods: {
    getGDPR () {
      if (process.browser) {
        return localStorage.getItem('GDPR:accepted', true)
      }
    },
    accept () {
      if (process.browser) {
        this.isOpen = false
        this.$root.$emit('DescerWhatsapp')
        this.$root.$emit('DescerTopo')
        localStorage.setItem('GDPR:accepted', true)
      }
    },
    deny () {
      if (process.browser) {
        this.isOpen = false
        this.$root.$emit('DescerWhatsapp')
        this.$root.$emit('DescerTopo')
        localStorage.setItem('GDPR:accepted', false)
      }
    },
    Politica () {
      this.$router.push('/politica-de-privacidade/')
    }
  }
}
</script>

<style scoped>
  .cookie{
    z-index: 100025;
    position: fixed;
    left: 0;
    bottom: 0;
    width: calc(100% - 100px);
    max-width: 450px;
  }
  .text-underline{
    text-decoration: underline;
  }
  .cookie__link{
    color: #ffffff;
    text-decoration: underline;
    transition: all .25s;
  }
  .cookie__link:hover{
    text-decoration: none
  }
  .div-cookie{
    box-shadow: 0 0.1rem 1rem rgba(0, 0, 0, 0.556) !important;
  }

  @media (max-width: 575.95px) {
    .div-cookie p, .div-cookie button{
      font-size: 13px;
    }
  }
</style>
