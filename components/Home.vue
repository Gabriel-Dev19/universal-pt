<template>
  <section>
    <div class="carousel_bg_home">
      <b-carousel
        id="carousel-home"
        fade
        no-hover-pause
        class="col-12 px-0 h-100"
      >
        <b-carousel-slide class="bg_home_1" />
        <b-carousel-slide class="bg_home_2" />
        <b-carousel-slide class="bg_home_3" />
      </b-carousel>
    </div>
    <div class="container align-self-end mt-5 pt-5 pt-xl-0">
      <div class="d-flex justify-content-center">
        <div class="">
          <img src="../assets/img/logo-universal-branca.webp" width="200" class="img-fluid" alt="">
        </div>
      </div>
      <h5 class="text-white text-center mb-0 text-uppercase mt-2 font-wide">
        Detetives particulares
      </h5>
      <div class="separation_home mx-auto col-5" />
      <h1 class="text-white font-wide fs-30 mt-4 col-7 mx-auto text-center text-uppercase">
        Agência de detetives particulares
      </h1>
      <p class="mx-auto col-8 fw-300 text-center text-white">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi iste deleniti
        dolore quos dicta illum in consectetur aspernatur voluptates culpa amet tempore, repellat
        quae eos odio vel. Assumenda!
      </p>
      <div class="d-flex mt-4 justify-content-center">
        <button class="button_home btn font-wide">
          {{ nameBtn }}
        </button>
      </div>
    </div>
    <div class="nav_telefones align-self-end d-none d-xl-block col-12">
      <div class="container">
        <div class="mae_telefones">
          <div v-for="telefone in telefones" :key="telefone.name" class="col_telefones">
            <a href="tel:">
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
          <a href="tel:">
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
  props: ['nameBtn'],
  data () {
    return {
      telefones: [
        { name: 'Florianópolis', numero: '(65) 3453-3453' },
        { name: 'Baln. Camboriú', numero: '(67) 3679-3685' },
        { name: 'Curitiba', numero: '(33) 3454-3455' },
        { name: 'Caçador', numero: '(44) 7567-5676' }
      ]
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

      .bg_home_1{
        background: linear-gradient(0deg, #000000dc 1%, #000000a4, #000000dc 99% ), url(../assets/img/detetive-examinando-evidencia.jpg) center center no-repeat;
        background-size: cover;
      }
      .bg_home_2{
        background: linear-gradient(0deg, #000000dc 1%, #000000a4, #000000dc 99% ), url(../assets/img/linhas-investigacao.jpg) center center no-repeat;
        background-size: cover;
      }
      .bg_home_3{
        background: linear-gradient(0deg, #000000dc 1%, #000000a4, #000000dc 99% ), url(../assets/img/mulher-com-lupa.jpg) center center no-repeat;
        background-size: cover;
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
    }
  }
</style>
