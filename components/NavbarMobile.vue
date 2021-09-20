<template>
  <header>
    <nav v-scroll="ScrollNavMobile" class="navbar nav fixed-top d-xl-none" :class="{'pt-not-scroll': !Nav_Scroll, 'py-3 bg-light shadow-nav': Nav_Scroll}">
      <div class="filha-nav d-flex justify-content-end">
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <a v-show="Show_Logo" href="" class="link_logo">
            <img src="../assets/img/logo-universal.webp" width="120" alt="Logo Universal detetives">
          </a>
        </transition>
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <div v-show="Show_Logo" class="circulo_branco" />
        </transition>
        <button class="btn d-flex justify-content-center align-items-center" :class="{'translate-button': Translate_button}" @click="Toggle_Nav">
          <ion-icon v-show="Toggle_Icon_Times" name="menu-outline" />
          <ion-icon v-show="!Toggle_Icon_Times" name="close-outline" />
        </button>
      </div>
      <transition enter-active-class="animate-show-nav" leave-active-class="animate-hide-nav">
        <div v-show="Hide_nav" class="nav-event">
          <h5 class="text-white mb-4 ml-3 pl-1">
            Menu
          </h5>
          <nuxt-link to="/" class="nuxt-link-mobile">
            Home
            <ion-icon name="arrow-forward-outline" />
          </nuxt-link>
          <nuxt-link to="/" class="nuxt-link-mobile">
            Sobre nós
            <ion-icon name="arrow-forward-outline" />
          </nuxt-link>
          <div class="nuxt-link-mobile">
            Serviços
            <ion-icon name="menu-outline" />
          </div>
          <div class="nuxt-link-mobile">
            Localidades atendidas
            <ion-icon name="menu-outline" />
          </div>
          <nuxt-link to="/" class="nuxt-link-mobile">
            Contate nossa equipe
            <ion-icon name="arrow-forward-outline" />
          </nuxt-link>
          <div class="nav_redes_sociais mt-4 ml-3 pl-1">
            <a v-for="items in redes_sociais" :key="items.icon" :href="items.linkTo">
              <ion-icon :name="items.icon" />
            </a>
          </div>
        </div>
      </transition>
    </nav>
  </header>
</template>
<script>
export default {
  data () {
    return {
      Nav_Scroll: false,
      Hide_nav: false,
      Show_Logo: false,
      Toggle_Icon_Times: true,
      Translate_button: false,

      redes_sociais: [
        { icon: 'logo-twitter', linkTo: '/' },
        { icon: 'logo-facebook', linkTo: '/' },
        { icon: 'logo-instagram', linkTo: '/' },
        { icon: 'logo-pinterest', linkTo: '/' },
        { icon: 'logo-youtube', linkTo: '/' }
      ]
    }
  },
  methods: {
    ScrollNavMobile () {
      if (document.body.classList.contains('overflow-hidden') === false) {
        if (window.scrollY > 10) {
          this.Nav_Scroll = true
          this.Show_Logo = true
        } else {
          this.Nav_Scroll = false
          this.Show_Logo = false
        }
      }
    },
    Toggle_Nav () {
      this.Translate_button = !this.Translate_button
      this.Toggle_Icon_Times = !this.Toggle_Icon_Times
      document.body.classList.toggle('overflow-hidden')
      if (window.scrollY > 10) {
        this.Hide_nav = !this.Hide_nav
        this.Nav_Scroll = true
        this.Show_Logo = !this.Show_Logo
      } else {
        this.Hide_nav = !this.Hide_nav
        this.Nav_Scroll = !this.Nav_Scroll
        this.Show_Logo = false
      }
    }
  }
}
</script>
<style lang="scss" scoped>
  @keyframes AnimateShowNav {
    from{
      transform: scale3d(0, 0, 0);
      transform-origin: calc(100% - 45px) 45px;
      border-radius: 50%;
    }
    to{
      transform: scale3d(1, 1, 1);
      transform-origin: 100% 0px;
      border-radius: 0%;
    }
  }
  .animate-show-nav{
    animation-name: AnimateShowNav;
    animation-duration: .5s;
  }
  .animate-hide-nav{
    animation-name: AnimateShowNav;
    animation-duration: .5s;
    animation-direction: reverse;
  }
  nav{
    transition: all .5s;

    &.shadow-nav{
      box-shadow: 0 0.1rem 0.3rem rgba(0, 0, 0, 0.234) !important;
    }

    &.pt-not-scroll{
      padding-top: 37px;
    }

    .filha-nav{
      width: 100%;
      position: relative;
      padding: 0 20px;

      .link_logo{
        position: absolute;
        top: -5px;
        left: 15px;
      }

      .circulo_branco{
        position: absolute;
        top: -5px;
        left: 28px;
        background-color: var(--light);
        z-index: -1;
        width: 91px;
        height: 87px;
        border-radius: 50%;
        box-shadow: 0 0.3rem 0.3rem rgba(0, 0, 0, 0.097) !important;
      }
    }

    button{
      height: 45px;
      width: 45px;
      border-radius: 50%;
      background-color: var(--azul);
      transition: transform .5s;

      ion-icon[name="menu-outline"]{
        min-width: 29px;
        color: white;
        font-size: 29px !important;
      }
      ion-icon[name="close-outline"]{
        min-width: 32px;
        color: white;
        font-size: 32px !important;
      }

      &.translate-button{
        transform: translateX(25px);
      }
    }

    .nav-event{
      position: absolute;
      height: 100vh;
      padding-top: 26px;
      width: 100%;
      top: 0px;
      right: 0px;
      z-index: -1;
      background-color: var(--azul);
      transition: all .5s;

      .nuxt-link-mobile{
        color: white;
        width: 100% !important;
        padding: 11px 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid #ffffffb4;
        font-size: 18px;

        ion-icon{
          color: #fff;
          min-width: 23px;
          font-size: 23px;
        }

        &:nth-child(2){
          border-top: 1px solid #ffffffb4;
        }
      }

      .nav_redes_sociais{
        display: flex;

        a{
          margin-right: 20px;
          position: relative;

          &:last-child{
            margin-right: 0 !important;
          }

          ion-icon{
            font-size: 25px;
            min-width: 25px;
            width: 100%;
            margin-bottom: -7px !important;
            color: white;
          }
        }
      }
    }
  }
</style>
