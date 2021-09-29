<template>
  <div v-scroll="ScrollBtnWhatsapp" class="mae_btn cursor-pointer" :class="{'hide_content': !ShowContent, 'show_content': ShowContent}" @click="ToggleWhats">
    <div class="content_btn">
      <div class="header_btn">
        <span v-show="ShowContent" class="times">
          &times;
        </span>
        <ion-icon class="cursor-pointer animate-whatsapp" name="logo-whatsapp" />
        <transition enter-active-class="animate_show_content_whatsapp">
          <h5 v-show="ShowContent" class="mb-0 font-wide" @click.stop="">
            Canal de atendimento
          </h5>
        </transition>
      </div>
      <transition enter-active-class="animate_show_content_whatsapp" leave-active-class="animate_hide_content_whatsapp">
        <div v-show="ShowContent" class="content_numeros" @click.stop="">
          <a v-for="item in numeros_whats" :key="item.name" :href="`https://wa.me/55${item.numeroLink}?text=Olá,+estou+visitando+o+site+da+Universal+Detetives+e+gostaria+de+receber+mais+informações`" target="_blank" class="pl-4 d-block">
            <span class="d-block text-grafite" style="font-weight: 600">
              <ion-icon class="text-azul" name="location-outline" /> {{ item.name }}
            </span>
            <div class="d-flex">
              <a class="link-seta cinza">
                {{ item.numero }}
                <div class="mae_seta">
                  <div class="seta">
                    <ion-icon name="chevron-forward-outline" />
                  </div>
                </div>
              </a>
            </div>
          </a>
        </div>
      </transition>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      ShowContent: false,
      numeros_whats: [
        {
          name: 'Santa Catarina',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Paraná',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Rio Grande do Sul',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'São Paulo',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Rio de Janeiro',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Minas Gerais',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Distrito Federal',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Mato Grosso do Sul',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        },
        {
          name: 'Goiás',
          numeroLink: '47991062096',
          numero: '+55 (47) 99106-2096'
        }
      ]
    }
  },
  created () {
    this.$root.$on('ShowWhats', () => {
      this.ToggleWhats()
    })
  },
  methods: {
    ScrollBtnWhatsapp () {
      if (window.scrollY) {
        this.ShowContent = false
      }
    },
    ToggleWhats () {
      this.ShowContent ? document.body.classList.remove('overflow-hidden') : document.body.classList.add('overflow-hidden')
      this.ShowContent = !this.ShowContent
    }
  }
}
</script>
<style lang="scss" scoped>
  // Aniamtions
  @keyframes AnimateShow {
    from{
      transform: scale3d(0, 0, 0);
    }

    to{
      transform: scale3d(1, 1, 1);
    }
  }

  .animate-whatsapp{
    animation-name: AnimateWhatsapp;
    -o-animation-name: AnimateWhatsapp;
    -moz-animation-name: AnimateWhatsapp;
    -webkit-animation-name: AnimateWhatsapp;
    animation-duration: 5s;
    -o-animation-duration: 5s;
    -moz-animation-duration: 5s;
    -webkit-animation-duration: 5s;
    animation-iteration-count: infinite;
    -o-animation-iteration-count: infinite;
    -moz-animation-iteration-count: infinite;
    -webkit-animation-iteration-count: infinite;
  }

  @keyframes AnimateWhatsapp {
    60% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }

    75% {
      transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -o-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -moz-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -webkit-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
    }

    87% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    90% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    93% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    96% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    99% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    100% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }
  }

  @-o-keyframes AnimateWhatsapp {
    60% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }

    75% {
      transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -o-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -moz-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -webkit-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
    }

    87% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    90% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    93% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    96% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    99% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    100% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }
  }

  @-moz-keyframes AnimateWhatsapp {
    60% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }

    75% {
      transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -o-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -moz-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -webkit-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
    }

    87% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    90% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    93% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    96% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    99% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    100% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }
  }

  @-webkit-keyframes AnimateWhatsapp {
    60% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }

    75% {
      transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -o-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -moz-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
      -webkit-transform: scale3d(1.1, 1.1, 1.1) rotate(20deg);
    }

    87% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    90% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    93% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    96% {
      transform: rotate(20deg);
      -o-transform: rotate(20deg);
      -moz-transform: rotate(20deg);
      -webkit-transform: rotate(20deg);
    }

    99% {
      transform: rotate(-20deg);
      -o-transform: rotate(-20deg);
      -moz-transform: rotate(-20deg);
      -webkit-transform: rotate(-20deg);
    }

    100% {
      transform: scale3d(1, 1, 1);
      -o-transform: scale3d(1, 1, 1);
      -moz-transform: scale3d(1, 1, 1);
      -webkit-transform: scale3d(1, 1, 1);
    }
  }

  .animate_show_content_whatsapp{
    animation-name: AnimateShow;
    animation-duration: .5s;
  }

  .animate_hide_content_whatsapp{
    animation-name: AnimateShow;
    animation-duration: .5s;
    animation-direction: reverse;
  }

  .mae_btn{
    position: fixed;
    bottom: 0;
    right: 0;
    padding: 15px 0 15px 15px;
    border-radius: 20px 0 0 0;
    box-shadow: 0 0.1rem 0.7rem rgba(0, 0, 0, 0.44) !important;
    background-color: white;
    min-height: 85px;
    min-width: 75px;
    max-height: calc(100vh - 130px);
    max-width: calc(100vw - 35px);
    z-index: 1000;
    transition: all .7s;

    &.show_content{
      width: 332px;
      height: 442px;
    }
    &.hide_content{
      height: 0;
      width: 0;
    }

    a:hover{
      text-decoration: none;
    }

    .content_btn{
      border: 1px solid transparent;
      height: 100%;
      cursor: default;

      .header_btn{
        position: relative;
        min-height: 45px;
        display: flex;
        align-items: center;

        ion-icon{
          position: absolute;
          top: 0;
          left: 0;
          font-size: 45px;
          min-width: 45px;
          color: var(--whatsapp);
        }

        .times{
          position: absolute;
          left: -47px;
          top: -10px;
          padding-right: 20px !important;
          font-size: 40px;
          cursor: pointer;
        }

        h5{
          width: calc(100% - 55px);
          margin-left: auto;
        }
      }

      .content_numeros{
        height: calc(100% - 60px);
        width: 100%;
        padding-bottom: 40px;
        margin-top: 28px;
        overflow-y: scroll;

        a{
          margin-top: 16px;

          &:first-child{
            margin-top: 0 !important;
          }
        }
      }
    }
  }
</style>
