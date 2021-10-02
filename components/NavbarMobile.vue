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
          <nuxt-link to="/" class="nuxt-link-mobile" @click.native="Toggle_Nav">
            Home
            <ion-icon name="arrow-forward-outline" />
          </nuxt-link>
          <nuxt-link to="/sobre" class="nuxt-link-mobile" @click.native="Toggle_Nav">
            Sobre nós
            <ion-icon name="arrow-forward-outline" />
          </nuxt-link>
          <div v-b-toggle.collapse-servicos class="nuxt-link-mobile">
            Serviços
            <ion-icon name="menu-outline" />
          </div>
          <b-collapse id="collapse-servicos" class="col-12 px-0">
            <div class="collapse-body">
              <nuxt-link
                v-for="items in LinksMobileCollapseServicos"
                :key="items.name"
                :to="items.routerTo"
                class="nuxt_link_mobile_collapse"
                @click.native="Toggle_Nav"
              >
                {{ items.name }}
                <ion-icon name="arrow-forward-outline" />
              </nuxt-link>
            </div>
          </b-collapse>
          <div v-b-toggle.collapse-localidades class="nuxt-link-mobile">
            Localidades atendidas
            <ion-icon name="menu-outline" />
          </div>
          <b-collapse id="collapse-localidades" class="col-12 px-0">
            <div class="collapse-body">
              <nuxt-link
                v-for="items in LinksMobileCollapseLocalidades"
                :key="items.name"
                :to="items.routerTo"
                class="nuxt_link_mobile_collapse"
                @click.native="Toggle_Nav"
              >
                {{ items.name }}
                <ion-icon name="arrow-forward-outline" />
              </nuxt-link>
            </div>
          </b-collapse>
          <a v-scroll-to="{ offset: -190, el: '#contato' }" class="nuxt-link-mobile" @click="Toggle_Nav">
            Contate nossa equipe
            <ion-icon name="arrow-forward-outline" />
          </a>
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
      ],

      LinksMobileCollapseServicos: [
        {
          name: 'Investigação conjugal',
          routerTo: '/servicos/investigacao-conjugal'
        },
        {
          name: 'Investigação empresarial',
          routerTo: '/servicos/investigacao-empresarial'
        },
        {
          name: 'Investigação politica',
          routerTo: '/servicos/investigacao-politica'
        },
        {
          name: 'Localização de pessoas',
          routerTo: '/servicos/localizacao-de-pessoas'
        },
        {
          name: 'Acompanhamento de filhos',
          routerTo: '/servicos/acompanhamento-de-filhos'
        },
        {
          name: 'Curso de detetive particular',
          routerTo: '/servicos/curso-de-detetive-particular'
        },
        {
          name: 'Celular VIP',
          routerTo: '/servicos/celular-VIP'
        }
      ],

      LinksMobileCollapseLocalidades: [
        { name: 'Santa Catarina', routerTo: '/detetive-particular-em-Santa-Catarina' },
        { name: 'Paraná', routerTo: '/detetive-particular-no-Parana' },
        { name: 'Rio Grande do Sul', routerTo: '/detetive-particular-no-Rio-Grande-do-Sul' },
        { name: 'São Paulo', routerTo: '/detetive-particular-em-Sao-Paulo' },
        { name: 'Rio de Janeiro', routerTo: '/detetive-particular-no-Rio-de-Janeiro' },
        { name: 'Distrito Federal', routerTo: '/detetive-particular-no-Distrito-Federal' },
        { name: 'Minas Gerais', routerTo: '/detetive-particular-em-Minas-Gerais' },
        { name: 'Mato Grosso do Sul', routerTo: '/detetive-particular-no-Mato-Grosso-do-Sul' },
        { name: 'Goiás', routerTo: '/detetive-particular-em-Goias' }
      ]
    }
  },
  mounted () {
    document.body.classList.remove('overflow-hidden')
    this.Hide_nav = false
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
      overflow-y: scroll;
      padding-bottom: 30px;

      .nuxt-link-mobile{
        color: white;
        width: 100% !important;
        padding: 11px 20px;
        display: flex;
        flex-wrap: wrap;
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

        &:focus{
          outline: none !important;
        }
      }

      .collapse-body{
        background-color: var(--azul_super_escuro);
        padding: 15px 20px 15px 30px;
        width: 100%;
        border-bottom: 1px solid #ffffffb4;

        .nuxt_link_mobile_collapse{
          margin-top: 10px;
          display: flex;
          align-items: center;
          justify-content: space-between;
          color: white;

          ion-icon{
            color: #fff;
            min-width: 18px;
            font-size: 18px;
          }

          &:first-child{
            margin-top: 0 !important;
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
