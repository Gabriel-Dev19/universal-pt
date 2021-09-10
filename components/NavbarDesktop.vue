<template>
  <header>
    <nav v-scroll="ScrollNav" :class="{'bg-light shadow-nav py-3': NavScroll, 'pt-5': !NavScroll}" class="nav navbar d-none d-xl-block fixed-top">
      <div class="container" :class="{'justify-content-between': !NavScroll, 'justify-content-end': NavScroll}">
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <a v-show="NavScroll" href="" class="link_logo">
            <img src="../assets/img/logo-universal.webp" width="130" alt="Logo Universal detetives">
          </a>
        </transition>
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <div v-show="NavScroll" class="circulo_branco" />
        </transition>
        <div class="nav_links" :class="{'animate__animated animate__slideInLeft': NavScroll, 'animate__animated animate__slideInRight': !NavScroll}">
          <nuxt-link to="/" class="nav-link" :class="{'text-white': !NavScroll}">
            Home
          </nuxt-link>
          <nuxt-link to="/sobre" class="nav-link" :class="{'text-white': !NavScroll}">
            Sobre nós
          </nuxt-link>
          <div class="nav-link cursor-pointer" :class="{'text-white': !NavScroll}">
            Serviços <ion-icon class="text-azul fs-18" style="margin-bottom: -4px" name="chevron-down-outline" />
          </div>
          <div class="nav-link cursor-pointer" :class="{'text-white': !NavScroll}">
            Localidades <ion-icon class="text-azul fs-18" style="margin-bottom: -4px" name="chevron-down-outline" />
          </div>
          <a href="" class="nav-link" :class="{'text-white': !NavScroll}">
            Fale conosco
          </a>
        </div>
        <transition enter-active-class="animate__animated animate__fadeInDown">
          <div v-show="!NavScroll" class="nav_redes_sociais">
            <a href="">
              <ion-icon name="logo-twitter" />
            </a>
            <a href="">
              <ion-icon name="logo-facebook" />
            </a>
            <a href="">
              <ion-icon name="logo-instagram" />
            </a>
            <a href="">
              <ion-icon name="logo-pinterest" />
            </a>
            <a href="">
              <ion-icon name="logo-youtube" />
            </a>
          </div>
        </transition>
      </div>
    </nav>
  </header>
</template>
<script>
export default {
  data () {
    return {
      NavScroll: false
    }
  },
  methods: {
    ScrollNav () {
      if (window.scrollY > 10) {
        this.NavScroll = true
      } else {
        this.NavScroll = false
      }
    }
  }
}
</script>
<style lang="scss" scoped>
  nav{
    transition: all .3s;

    &.shadow-nav{
      box-shadow: 0 0.1rem 0.3rem rgba(0, 0, 0, 0.234) !important;
    }

    .container{
      display: flex;
      align-items: center;
      transition: all .3s;
      position: relative;

      .link_logo{
        position: absolute;
        top: 0;
        left: 0;
      }

      .circulo_branco{
        position: absolute;
        top: 0;
        left: 12px;
        background-color: var(--light);
        z-index: -1;
        width: 105px;
        height: 90px;
        border-radius: 50%;
        box-shadow: 0 0.3rem 0.3rem rgba(0, 0, 0, 0.097) !important;
      }

      .nav_links{
        display: flex;

        .nav-link{
          color: var(--grafite);
          letter-spacing: 1.5px;
          position: relative;
          padding-left: 0 !important;
          padding-right: 0 !important;
          margin-right: 40px;
          text-transform: uppercase;
          font-weight: 300;
          font-size: 14px;
          font-family: 'Audiowide', cursive;

          &:last-child{
            margin-right: 0 !important;
          }

          &:not(div){
            &::after{
              content: '';
              position: absolute;
              left: 0;
              bottom: 2px;
              width: 0%;
              height: 2px;
              background-color: var(--azul);
              transition: all .3s;
            }

            &:hover{
              &::after{
                width: 100%;
              }
            }
          }

          &.nuxt-link-exact-active{
            &::after{
              width: 100%;
            }
          }
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

          &::after{
            content: '';
            position: absolute;
            left: 0;
            bottom: -7px;
            width: 0%;
            height: 2px;
            background-color: var(--azul);
            transition: all .3s;
          }

          &:hover{
            &::after{
              width: 100%;
            }
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
