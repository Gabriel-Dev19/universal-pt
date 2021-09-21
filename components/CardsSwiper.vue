<template>
  <section>
    <div class="container" @mouseenter="stopSlide" @mouseleave="runSlide">
      <div class="box_titulo_explore px-1">
        <div class="row titulo_swiper mx-0">
          <Badge name="nos conheça" />
          <h2 class="col-12 px-0">
            Explore nosso trabalho!
          </h2>
        </div>
        <div>
          <button class="btn p-0 button-next">
            <ion-icon name="arrow-forward-circle-outline" />
          </button>
        </div>
      </div>
      <swiper
        id="swiper-explore"
        ref="swiperCards"
        class="swiper py-2 px-1"
        :options="swiperOption"
      >
        <swiper-slide
          v-for="swipers in slides"
          :key="swipers.title"
        >
          <div class="circulo_icon">
            <ion-icon :name="swipers.icon" />
          </div>
          <h6>
            {{ swipers.title }}
          </h6>
          <p>
            {{ swipers.description }}
          </p>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import Badge from './parts/Badge.vue'

export default {
  // eslint-disable-next-line vue/component-definition-name-casing
  name: 'swiper-example-grab-cursor',
  title: 'Grab cursor',
  components: {
    Swiper,
    SwiperSlide,
    Badge
  },
  data () {
    return {
      swiperOption: {
        slidesPerView: 'auto',
        spaceBetween: 25,
        grabCursor: true,
        loop: true,
        navigation: {
          nextEl: '.button-next'
        },
        autoplay: {
          delay: 1500,
          disableOnInteraction: false
        }
      },
      slides: [
        {
          title: 'Investigação empresarial',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'cash-outline'
        },
        {
          title: 'Investigação conjugal',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'heart-dislike'
        },
        {
          title: 'Localização de pessoas',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'locate-outline'
        },
        {
          title: 'Filhos rebeldes',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'man-outline'
        },
        {
          title: 'Curso de detetive',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'school'
        },
        {
          title: 'Investigação política',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'document-attach-outline'
        },
        {
          title: 'Celular VIP',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'phone-portrait'
        },
        {
          title: 'Coleta de provas',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'finger-print-outline'
        },
        {
          title: 'Campanas',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'footsteps-outline'
        }
      ]
    }
  },
  methods: {
    stopSlide () {
      this.$refs.swiperCards.$swiper.autoplay.stop()
    },
    runSlide () {
      this.$refs.swiperCards.$swiper.autoplay.start()
    }
  }
}
</script>

<style lang="scss" scoped>
  section{
    padding: 100px 0 150px 0;
    background: linear-gradient(180deg, var(--cinza_claro), #ffffff00);
  }
  .box_titulo_explore{
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    .titulo_swiper{
      max-width: 320px;
    }

    ion-icon{
      font-size: 48px;
      color: var(--azul);
      --ionicon-stroke-width: 18px;
    }
  }
  .swiper{
    margin-top: 30px;

    .swiper-wrapper{
      .swiper-slide{
        padding: 25px;
        border-radius: 20px;
        background-color: white;
        color: var(--grafite);
        width: 300px;
        box-shadow: 0 0.1rem 0.5rem rgba(0, 0, 0, 0.309) !important;

        .circulo_icon{
          display: flex;
          justify-content: center;
          align-items: center;
          width: 48px;
          height: 48px;
          border-radius: 50%;
          background-color: var(--cinza_claro);

          ion-icon{
            font-size: 28px;
          }
        }

        h6{
          margin-top: 18px;
          font-weight: 600;
          font-size: 18px;
        }

        p{
          font-size: 14px;
          margin-bottom: 0 !important;
        }
      }
      .swiper-slide[data-swiper-slide-index="1"],
      .swiper-slide[data-swiper-slide-index="4"],
      .swiper-slide[data-swiper-slide-index="6"]{
        background-color: var(--azul);
        color: var(--white);

        .circulo_icon{
          background-color: var(--azul_super_escuro);
        }
      }
    }
  }
</style>
