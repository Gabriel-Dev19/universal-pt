<template>
  <section>
    <div class="carousel_bg_home">
      <b-carousel
        id="carousel-home"
        fade
        no-hover-pause
        class="col-12 px-0 h-100"
      >
        <b-carousel-slide class="bg_home_1">
          <img src="../assets/img/detetive-examinando-evidencia.webp" alt="">
          <div class="gradiente" />
        </b-carousel-slide>
        <b-carousel-slide class="bg_home_2">
          <img src="../assets/img/linhas-investigacao.webp" alt="">
          <div class="gradiente" />
        </b-carousel-slide>
        <b-carousel-slide class="bg_home_3">
          <img src="../assets/img/mulher-com-lupa.webp" alt="">
          <div class="gradiente" />
        </b-carousel-slide>
      </b-carousel>
    </div>
    <div class="container align-self-end mt-4 pt-4 mt-xl-5 pt-xl-0">
      <div class="d-flex justify-content-center">
        <div class="">
          <img src="../assets/img/logo-universal-branca.webp" width="200" class="img-fluid" alt="">
        </div>
      </div>
      <h5 class="text-white text-center mb-0 text-uppercase mt-2 font-wide">
        Detetives particulares
      </h5>
      <div class="separation_home mx-auto col-5" />
      <h1 class="text-white font-wide mt-4 px-0 col-md-8 mx-auto text-center text-uppercase">
        {{ titlePrincipal }}
      </h1>
      <p v-if="description.length > 1" class="mx-auto px-0 col-md-8 fw-300 text-center text-white" v-html="description" />
      <div v-if="nameBtn.length > 1" class="d-flex mt-4 justify-content-center">
        <button v-scroll-to="optionsScroll" class="button_home btn font-wide">
          {{ nameBtn }}
        </button>
      </div>
    </div>
    <div class="nav_telefones align-self-end col-12">
      <div class="container">
        <div class="mae_telefones d-none d-xl-flex">
          <div v-for="telefone in telefones" :key="telefone.name" class="col_telefones">
            <a :href="`tel:${telefone.href}`">
              <ion-icon name="call-outline" />
              <div class="separation_telefones" />
              <div>
                <h6> {{ telefone.name }} </h6>
                <span>
                  {{ telefone.numero }}
                </span>
              </div>
            </a>
          </div>
        </div>
        <div class="col_whatsapp">
          <a class="cursor-pointer" @click="$root.$emit('ShowWhats')">
            <ion-icon name="logo-whatsapp" />
            <div class="separation_telefones" />
            <h6 class="font-wide text-uppercase">
              Mensagem
            </h6>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: {
    nameBtn: {
      type: String,
      default: ''
    },
    titlePrincipal: {
      type: String,
      default: 'Agência de detetives particulares'
    },
    description: {
      type: String,
      default: `Para a Universal Agência de Detetives sempre haverá uma <br>
      solução que estará à altura das suas necessidades.`
    },
    hashBtn: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      telefones: [
        { name: 'Florianópolis', numero: '(48) 4052-8425', href: '4840528425' },
        { name: 'Baln. Camboriú', numero: '(47) 4054-9580', href: '4740549580' },
        { name: 'Curitiba', numero: '(41) 4063-9171', href: '4140639171' },
        { name: 'Caçador', numero: '(49) 3240-0977', href: '4932400977' }
      ],
      Quantidade_retira_hash: 0,
      optionsScroll: {
        el: '#' + this.hashBtn,
        offset: -190
      }
    }
  }
}
</script>
<style lang="scss" scoped>
  section{
    height: 100vh;
    min-height: 750px;
    max-height: 830px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    position: relative;

    @media (min-width: 1200px) {
      align-items: unset;
    }

    // Aniamtes
    @keyframes AnimateTelefones {
      0%{
        transform: rotate(0deg);
      }
      25%{
        transform: rotate(15deg);
      }
      50%{
        transform: rotate(-15deg);
      }
      75%{
        transform: rotate(15deg);
      }
      100%{
        transform: rotate(0deg);
      }

    }

    .carousel_bg_home{
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      z-index: -1;

      .bg_home_1 img,
      .bg_home_2 img,
      .bg_home_3 img{
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

      .bg_home_1,
      .bg_home_2,
      .bg_home_3{
        position: relative;

        .gradiente{
          width: 100%;
          height: 100%;
          position: absolute;
          top: 0;
          left: 0;
          background: linear-gradient(0deg, #000000dc 1%, #000000a4, #000000dc 99% );
        }
      }
    }

    .nav_telefones{
      padding-bottom: 25px;

      .container{
        display: flex;
        align-items: center;
        justify-content: space-between;

        .mae_telefones{
          display: flex;

          .col_telefones{
            width: auto;
            margin-right: 80px;

            &:last-child{
              margin-right: 0 !important;
            }

            a{
              color: white;
              display: flex;
              justify-content: center;
              align-items: center;

              .separation_telefones{
                height: 30px;
                width: 1px;
                background-color: var(--azul);
                opacity: 0.7;
                margin-left: 10px;
                margin-right: 14px;
              }

              &:hover{
                text-decoration: none;
                ion-icon{
                  animation-name: AnimateTelefones;
                  animation-duration: .8s;
                  color: var(--azul);
                }
              }

              ion-icon{
                font-size: 26px;
                min-width: 26px;
                margin-bottom: 2px;
                transition: all .3s;
                --ionicon-stroke-width: 20px;
              }

              h6{
                font-weight: 400;
                font-size: 15px;
                margin-bottom: 0 !important;
              }

              span{
                font-weight: 300;
                font-size: 15px;
              }
            }
          }
        }

        .col_whatsapp{
          width: auto;

          a{
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;

            .separation_telefones{
              height: 30px;
              width: 1px;
              background-color: var(--azul);
              opacity: 0.7;
              margin-left: 10px;
              margin-right: 14px;
            }

            &:hover{
              text-decoration: none;
              ion-icon{
                animation-name: AnimateTelefones;
                animation-duration: .8s;
                color: var(--azul);
              }
            }

            ion-icon{
              font-size: 26px;
              min-width: 26px;
              margin-bottom: 2px;
              transition: all .3s;
              --ionicon-stroke-width: 20px;
            }

            h6{
              font-weight: 400;
              font-size: 17px;
              letter-spacing: 1.3px;
              margin-bottom: 0 !important;
            }
          }
          }

      }
    }

    .container{
      .separation_home{
        height: 1px;
        background-color: var(--azul);
        opacity: 0.8;
        margin-top: 20px;
        margin-bottom: 20px;
      }

      p{
        font-size: 15px;
      }

      .button_home{
        background: transparent;
        border-radius: 30px;
        border: 2px solid var(--azul);
        color: white;
        font-size: 15px;
        text-transform: uppercase;
        letter-spacing: 0.6px;
        word-spacing: 3px;
        padding: 10px 30px;

        &:hover{
          background-color: var(--azul);
        }
      }

      h5{
        @media (max-width: 576px) {
          &{
            font-size: 17px;
          }
        }
      }

      h1{
        font-size: 30px;

        @media (max-width: 576px) {
          &{
            font-size: 23px;
          }
        }
      }
    }
  }
</style>
