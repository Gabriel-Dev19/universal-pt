<template>
  <header>
    <nav v-scroll="ScrollNav" :class="{'bg-light shadow-nav py-3': Nav_Scroll, 'pt-5': !Nav_Scroll}" class="nav navbar d-none d-xl-block fixed-top">
      <div class="container" :class="{'justify-content-between': !Nav_Scroll, 'justify-content-end': Nav_Scroll}">
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <a v-show="Nav_Scroll" href="" class="link_logo">
            <img src="../assets/img/logo-universal.webp" width="130" alt="Logo Universal detetives">
          </a>
        </transition>
        <transition enter-active-class="animate__animated animate__fadeInUp">
          <div v-show="Nav_Scroll" class="circulo_branco" />
        </transition>
        <div class="nav_links" :class="{'animate__animated animate__slideInLeft': Nav_Scroll, 'animate__animated animate__slideInRight': !Nav_Scroll}">
          <nuxt-link to="/" class="nav-link" :class="{'text-white': !Nav_Scroll}">
            Home
          </nuxt-link>
          <nuxt-link to="/sobre" class="nav-link" :class="{'text-white': !Nav_Scroll}">
            Sobre nós
          </nuxt-link>
          <div
            class="nav-link cursor-pointer position-relative"
            :class="{'text-white': !Nav_Scroll}"
            @mouseenter="Shown_Dropdown_Servicos"
            @mouseleave="Hide_Dropdown_Servicos"
          >
            Serviços <ion-icon class="text-azul fs-18" style="margin-bottom: -4px" name="chevron-down-outline" />
            <transition enter-active-class="enter_animate_dropdown" leave-active-class="leave_animate_dropdown">
              <div
                v-show="Show_Dropdown_Servicos"
                class="dropdown-servicos"
                :class="{'position-right': Nav_Scroll}"
              >
                <div class="box_content">
                  <nuxt-link v-for="items in items_servicos" :key="items.name" :to="items.routeTo" class="btn links_box_dropdown">
                    {{ items.name }}
                    <div class="circulo_link">
                      <ion-icon name="chevron-forward-outline" />
                    </div>
                  </nuxt-link>
                </div>
              </div>
            </transition>
          </div>
          <div
            class="nav-link cursor-pointer"
            :class="{'text-white': !Nav_Scroll}"
            @mouseenter="Shown_Dropdown_Localidades"
            @mouseleave="Hide_Dropdown_Localidades"
          >
            Localidades <ion-icon class="text-azul fs-18" style="margin-bottom: -4px" name="chevron-down-outline" />
            <transition enter-active-class="enter_animate_dropdown" leave-active-class="leave_animate_dropdown">
              <div
                v-show="Show_Dropdown_Localidades"
                class="dropdown-localidades"
                :class="{'position-right': Nav_Scroll}"
              >
                <div class="box_content">
                  <nuxt-link v-for="items in items_localidades" :key="items.name" :to="items.routeTo" class="btn links_box_dropdown">
                    {{ items.name }}
                    <div class="circulo_link">
                      <ion-icon name="chevron-forward-outline" />
                    </div>
                  </nuxt-link>
                </div>
              </div>
            </transition>
          </div>
          <a href="" class="nav-link" :class="{'text-white': !Nav_Scroll}">
            Fale conosco
          </a>
        </div>
        <transition enter-active-class="animate__animated animate__fadeInDown">
          <div v-show="!Nav_Scroll" class="nav_redes_sociais">
            <a v-for="items in redes_sociais" :key="items.icon" :href="items.linkTo">
              <ion-icon :name="items.icon" />
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
      Nav_Scroll: false,
      Show_Dropdown_Servicos: false,
      Show_Dropdown_Localidades: false,
      Time_Espera_Dropdown_Servicos: undefined,
      Time_Espera_Dropdown_Localidades: undefined,
      items_servicos: [
        { name: 'Investigação empresarial', routeTo: '/investigacao-empresarial' },
        { name: 'Investigação conjugal', routeTo: '/investigacao-conjugal' },
        { name: 'Investigação política', routeTo: '/investigacao-politica' },
        { name: 'Localização de pessoas', routeTo: '/localizacao-de-pessoas' },
        { name: 'Curso de detetive particular', routeTo: '/curso-de-detetive-particular' },
        { name: 'Acompanhamento de filhos', routeTo: '/acompanhamento-de-filhos' },
        { name: 'Celular VIP', routeTo: '/celular-VIP' }
      ],
      items_localidades: [
        { name: 'Santa Catarina', routeTo: '/investigacao-empresarial' },
        { name: 'Paraná', routeTo: '/investigacao-conjugal' },
        { name: 'Rio Grande do Sul', routeTo: '/investigacao-politica' },
        { name: 'São Paulo', routeTo: '/localizacao-de-pessoas' },
        { name: 'Rio de Janeiro', routeTo: '/curso-de-detetive-particular' },
        { name: 'Distrito Federal', routeTo: '/celular-VIP' },
        { name: 'Minas Gerais', routeTo: '/curso-de-detetive-particular' },
        { name: 'Mato Grosso do Sul', routeTo: '/acompanhamento-de-filhos' },
        { name: 'Goiás', routeTo: '/acompanhamento-de-filhos' }
      ],
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
    ScrollNav () {
      if (window.scrollY > 10) {
        this.Nav_Scroll = true
        this.Show_Dropdown_Servicos = false
      } else {
        this.Nav_Scroll = false
      }
    },
    Shown_Dropdown_Servicos () {
      this.Show_Dropdown_Servicos = true
      this.Show_Dropdown_Localidades = false
      clearTimeout(this.Time_Espera_Dropdown)
    },
    Hide_Dropdown_Servicos () {
      this.Time_Espera_Dropdown = setTimeout(() => {
        this.Show_Dropdown_Servicos = false
      }, 300)
    },

    Shown_Dropdown_Localidades () {
      this.Show_Dropdown_Localidades = true
      this.Show_Dropdown_Servicos = false
      clearTimeout(this.Time_Espera_Dropdown_Localidades)
    },
    Hide_Dropdown_Localidades () {
      this.Time_Espera_Dropdown_Localidades = setTimeout(() => {
        this.Show_Dropdown_Localidades = false
      }, 300)
    }
  }
}
</script>
<style lang="scss" scoped>
  // Animations
  @keyframes AnimateEnterDropdown {
    from{
      transform: scale3d(0.95, 0.95, 0.95);
      opacity: 0;
    }
    to{
      transform: scale3d(1, 1, 1);
      opacity: 1;
    }
  }
  .enter_animate_dropdown{
    animation-name: AnimateEnterDropdown;
    animation-duration: .1s;
    animation-timing-function: ease-in;
  }
  .leave_animate_dropdown{
    animation-name: AnimateEnterDropdown;
    animation-duration: .1s;
    animation-direction: reverse;
    animation-timing-function: ease-in;
  }

  // Css Navbar
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

        .dropdown-servicos{
          position: absolute;
          top: 30;
          left: -30px;

          &.position-right{
            right: -30px !important;
            left: unset !important;
          }

          .box_content{
            margin-top: 15px;
            width: 350px;
            display: flex;
            flex-wrap: wrap;
            padding: 15px 8px;
            justify-content: center;
            background-color: var(--azul_escuro);
            border-radius: 20px;

            .links_box_dropdown{
              color: white;
              display: flex;
              margin-top: 5px;
              align-items: center;
              padding: 3px 3px 3px 10px;
              width: 100%;
              border-radius: 30px;
              justify-content: space-between;
              text-transform: capitalize;
              text-align: left !important;
              font-weight: 500;
              letter-spacing: 0.4px;
              transition: all .3s;
              font-family: 'Montserrat', sans-serif;

              &:first-child{
                margin-top: 0 !important;
              }

              .circulo_link{
                margin-left: 10px;
                min-width: 30px;
                display: flex;
                justify-content: center;
                align-items: center;
                min-height: 30px;
                border-radius: 50%;
                background-color: white;

                ion-icon{
                  font-size: 20px;
                  color: var(--grafite);
                  margin-left: 3px;
                }
              }

              &:hover{
                background-color: white;
                color: var(--grafite);
                padding: 3px 3px 3px 18px;

                .circulo_link{
                  background-color: var(--azul_escuro);

                  ion-icon{
                    color: white;
                  }
                }
              }

              &.nuxt-link-exact-active{
                background-color: white;
                color: var(--grafite);
                padding: 3px 3px 3px 18px;

                .circulo_link{
                  background-color: var(--azul_escuro);

                  ion-icon{
                    color: white;
                  }
                }
              }
            }
          }
        }

        .dropdown-localidades{
          position: absolute;
          top: 30;
          left: -30px;

          &.position-right{
            right: -30px !important;
            left: unset !important;
          }

          .box_content{
            margin-top: 15px;
            width: 280px;
            display: flex;
            flex-wrap: wrap;
            padding: 15px 8px;
            justify-content: center;
            background-color: var(--azul_escuro);
            border-radius: 20px;

            .links_box_dropdown{
              color: white;
              display: flex;
              margin-top: 5px;
              align-items: center;
              padding: 3px 3px 3px 10px;
              width: 100%;
              border-radius: 30px;
              justify-content: space-between;
              text-transform: capitalize;
              text-align: left !important;
              font-weight: 500;
              letter-spacing: 0.4px;
              transition: all .3s;
              font-family: 'Montserrat', sans-serif;

              &:first-child{
                margin-top: 0 !important;
              }

              .circulo_link{
                margin-left: 10px;
                min-width: 30px;
                display: flex;
                justify-content: center;
                align-items: center;
                min-height: 30px;
                border-radius: 50%;
                background-color: white;

                ion-icon{
                  font-size: 20px;
                  color: var(--grafite);
                  margin-left: 3px;
                }
              }

              &:hover{
                background-color: white;
                color: var(--grafite);
                padding: 3px 3px 3px 18px;

                .circulo_link{
                  background-color: var(--azul_escuro);

                  ion-icon{
                    color: white;
                  }
                }
              }

              &.nuxt-link-exact-active{
                background-color: white;
                color: var(--grafite);
                padding: 3px 3px 3px 18px;

                .circulo_link{
                  background-color: var(--azul_escuro);

                  ion-icon{
                    color: white;
                  }
                }
              }
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
