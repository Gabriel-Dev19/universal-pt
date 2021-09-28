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
              <img :src="item.img" alt="">
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
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Silva',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Gabriel',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Alguma',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Coisa',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Alberto',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          name: 'José Goiás',
          profission: 'Gerente de hotel',
          comment: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quibusdam vero vitae nostrum a ex,
              officiis laboriosam, quas nobis, nulla officia voluptatibus maiores`
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
            margin-top: -50px;
            overflow: hidden;

            img{
              height: 100%;
              width: 100%;
              object-fit: cover;
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
