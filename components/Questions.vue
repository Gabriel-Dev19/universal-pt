<template>
  <section>
    <div class="container">
      <div class="col-12 mb-5 row justify-content-between align-items-end mx-auto px-0">
        <div class="titulo_functions row mx-0">
          <Badge name="feedbacks" />
          <h2 class="col-12 pl-0">
            Veja o que as pessoas dizem sobre nós.
          </h2>
        </div>
        <div class="d-flex justify-content-end col-12 ml-auto pl-0 mt-4 mt-md-0 passadores">
          <button class="btn prev-slide-questions p-0">
            <ion-icon name="arrow-back-circle-outline" />
          </button>
          <button class="btn next-slide-questions ml-3 p-0">
            <ion-icon name="arrow-forward-circle-outline" />
          </button>
        </div>
      </div>
      <div class="quadradro-azul" />
    </div>
    <div class="mae_slides" @mouseenter="stopSlide" @mouseleave="runSlide">
      <swiper id="swiper-questions" ref="swiperQuestions" class="swiper" :options="swiperOption">
        <swiper-slide v-for="item in profiles" :key="item.name">
          <div class="content-swiper">
            <div class="circulo-profile">
              <ion-icon name="person-outline" />
            </div>
            <div class="mt-2 d-flex">
              <div class="col px-0">
                <h5 class="mb-0">
                  {{ item.name }}
                </h5>
                <span> {{ item.profission }} </span>
              </div>
              <div class="col px-0 ml-3 pt-1 d-flex justify-content-end">
                <ion-icon name="star" />
                <ion-icon name="star" />
                <ion-icon name="star" />
                <ion-icon name="star" />
                <ion-icon name="star" />
              </div>
            </div>
            <p class="mt-3">
              {{ item.comment }}
            </p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import Badge from './parts/Badge.vue'
import 'swiper/css/swiper.css'

export default {
  name: 'SwiperExample3dCoverflow',
  title: '3D Coverflow effect',
  components: {
    Swiper,
    SwiperSlide,
    Badge
  },
  data () {
    return {
      swiperOption: {
        effect: 'coverflow',
        grabCursor: true,
        centeredSlides: true,
        spaceBetween: 45,
        initialSlide: 1,
        slidesPerView: 'auto',
        loop: true,
        coverflowEffect: {
          rotate: 35,
          stretch: 0,
          depth: 100,
          modifier: 1,
          slideShadows: false
        },
        autoplay: {
          delay: 1500,
          disableOnInteraction: false
        },
        navigation: {
          nextEl: '.next-slide-questions',
          prevEl: '.prev-slide-questions'
        }
      },
      profiles: [
        {
          name: 'Sofia H.',
          profission: 'Corretora de imóveis',
          comment: `(...) A vida continua... é triste constatar que em 20 anos nunca conheci realmente o meu marido...
          Apesar de estar arrasada com o resultado, só tenho a agradecer vocês! Caso alguma amiga minha precise dos
          serviços de detetives, com certeza indicarei a Universal Detetives!`
        },
        {
          name: 'Felipe J.',
          profission: 'Product Manager',
          comment: `(...) Excelente trabalho! No início estava relutante em contratar este tipo de serviço,
          mas fiquei bastante satisfeito! Quando voltar a viajar já sei a quem recorrer! Se precisarem
          de alguma coisa que possa ajudar, estou à disposição! (...)`
        },
        {
          name: 'Antônio M.',
          profission: 'Gerente de empresa',
          comment: `(...) Agradecemos imensamente o trabalho de vocês. A administração estava bastante
          apreensiva em relação ao que o indivíduo estava fazendo, porém tudo ficou altamente esclarecido.
          Caso necessitemos novamente, a vossa agência será uma referência. Obrigado!`
        }
      ]
    }
  },
  methods: {
    stopSlide () {
      this.$refs.swiperQuestions.$swiper.autoplay.stop()
    },
    runSlide () {
      this.$refs.swiperQuestions.$swiper.autoplay.start()
    }
  }
}
</script>

<style lang="scss" scoped>

section{
  margin-top: 150px;
  .quadradro-azul{
    height: 250px;
    width: 100%;
    background-color: var(--azul);
    border-radius: 25px;
  }

  .titulo_functions{
    max-width: 400px;
  }

  .passadores{
    max-width: 200px !important;

    ion-icon{
      color: var(--azul);
      min-width: 45px;
      font-size: 45px;
      --ionicon-stroke-width: 19px;
    }
  }

  .mae_slides {
    margin-top: -270px;
    width: 100%;
    height: 450px;
    padding-top: 50px;
    padding-bottom: 20px;

    .swiper {
      height: 100%;
      width: 100%;
      padding-top: 40px;
      padding-bottom: 60px !important;

      .swiper-wrapper{
        height: 100%;
        padding-bottom: 40px !important;
      }

      .swiper-slide {
        border-radius: 20px;
        box-shadow: 0 0.1rem 1rem rgba(0, 0, 0, 0.35) !important;
        width: 430px;
        height: min-content !important;
        background-color: white;
        transform: scale3d(0.9, 0.9, 0.9) !important;

        @media (max-width: 576px) {
          width: 85%;
        }

        .content-swiper{
          padding: 25px;
          height: 100%;
          width: 100%;
          opacity: 0.5;
          transition: all .3s;

          .circulo-profile{
            width: 65px;
            height: 65px;
            border-radius: 50%;
            border: 4px solid white;
            background-color: #e6e6e6;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: -50px;
            overflow: hidden;

            ion-icon{
              font-size: 35px;
              min-width: 35px;
            }
          }

          h5{
            font-weight: 600;
          }

          span{
            font-size: 14px;
          }

          p{
            font-size: 15px;
            margin-bottom: 0 !important;
          }

          ion-icon{
            color: var(--azul_escuro);
            font-size: 20px;
            min-width: 20px;
            margin-right: 10px;

            &:last-child{
              margin-right: 0 !important;
            }
          }
        }
      }
      .swiper-slide-active{
        transform: scale3d(1, 1, 1) !important;
        .content-swiper{
          opacity: 1;
        }
      }
    }
  }
}

</style>
