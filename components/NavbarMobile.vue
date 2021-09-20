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
        <button class="btn d-flex justify-content-center align-items-center" @click="Toggle_Nav">
          <ion-icon v-show="Toggle_Icon_Times" name="menu-outline" />
          <ion-icon v-show="!Toggle_Icon_Times" name="close-outline" />
        </button>
      </div>
      <transition enter-active-class="animate-show-nav" leave-active-class="animate-hide-nav">
        <div v-show="Hide_nav" class="nav-event" />
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
      Toggle_Icon_Times: true
    }
  },
  methods: {
    ScrollNavMobile () {
      if (window.scrollY > 10) {
        this.Nav_Scroll = true
        this.Show_Logo = true
      } else {
        this.Nav_Scroll = false
        this.Show_Logo = false
      }
    },
    Toggle_Nav () {
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
    }

    .nav-event{
      position: absolute;
      height: 100vh;
      width: 100%;
      top: 0px;
      right: 0px;
      z-index: -1;
      background-color: var(--azul);
      transition: all .5s;

      &.if-hide-navbar{
        top: 55px;
        right: 50px;
        border-radius: 50%;
      }

      &.if-show-navbar{
        top: 0px;
        right: 0px;
        border-radius: 0%;
      }
    }
  }
</style>
