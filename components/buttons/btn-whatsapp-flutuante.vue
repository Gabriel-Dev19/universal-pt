<template>
  <div class="mae_btn cursor-pointer" :class="{'hide_content': !ShowContent, 'show_content': ShowContent}" @click="ToggleWhats">
    <div class="content_btn">
      <div class="header_btn">
        <span v-show="ShowContent" class="times">
          &times;
        </span>
        <div class="logo-whats">
          <ion-icon class="cursor-pointer animate-whatsapp" name="logo-whatsapp" />
          <div v-show="!ShowContent" class="mt-1">
            <span class="d-block" style="font-weight: 400; font-size: 10px;">Mande uma</span>
            <span class="d-block" style="font-weight: 700; font-size: 11px;">Mensagem</span>
          </div>
        </div>
        <transition enter-active-class="animate_show_content_whatsapp">
          <div v-show="ShowContent" class="mae_texto">
            <h5 class="mb-1 font-wide" @click.stop="">
              Canal de atendimento
            </h5>
            <p class="small mb-1">
              Fale com um especialista na sua região.
            </p>
            <div class="d-flex small align-items-center">
              <div class="bolinha-verde" />
              <b>Atendimento 24h</b>
            </div>
          </div>
        </transition>
      </div>
      <hr>
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
    this.$root.$on('ShowWhatsRemote', () => {
      this.ShowWhats()
    })
  },
  methods: {
    ToggleWhats () {
      this.ShowContent = !this.ShowContent
    },
    ShowWhats () {
      this.ShowContent = true
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

  @keyframes animateBolinhaOn {
    from{
      transform: scale3d(1, 1, 1);
    }
    50%{
      transform: scale3d(0.5, 0.5, 0.5);
    }
    to{
      transform: scale3d(1, 1, 1);
    }
  }

  .mae_btn{
    position: fixed;
    bottom: 0;
    right: 0;
    padding: 10px 0 10px 10px;
    border-radius: 20px 0 0 0;
    box-shadow: 0 0.1rem 0.7rem rgba(0, 0, 0, 0.44) !important;
    background-color: white;
    min-height: 110px;
    min-width: 80px;
    max-height: calc(100vh - 130px);
    max-width: calc(100vw - 35px);
    z-index: 1000;
    transition: all .7s;

    &.show_content{
      width: 342px;
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

        .logo-whats{
          position: absolute;
          top: 0;
          left: 0;
          cursor: pointer;

          ion-icon{
            font-size: 45px;
            min-width: 45px;
            color: var(--whatsapp);
          }
        }

        .times{
          position: absolute;
          left: -42px;
          top: -10px;
          padding-right: 20px !important;
          font-size: 40px;
          cursor: pointer;
        }

        .mae_texto{
          width: calc(100% - 55px);
          margin-left: auto;

          p{
            line-height: 15px;
          }

          .bolinha-verde{
            width: 12px;
            height: 12px;
            border-radius: 50%;
            margin-right: 5px;
            margin-bottom: 0.5px;
            background-color: var(--success);
            animation-name: animateBolinhaOn;
            animation-duration: 1s;
            animation-iteration-count: infinite;
          }
        }
      }

      .content_numeros{
        height: calc(100% - 90px);
        width: 100%;
        padding-bottom: 40px;
        margin-top: 18px;
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
