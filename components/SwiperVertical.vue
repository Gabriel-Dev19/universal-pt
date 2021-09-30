<template>
  <section>
    <div class="container">
      <div class="col-12 mb-5 row justify-content-between align-items-center mx-auto px-0">
        <div class="titulo_functions row mx-0">
          <Badge name="acredite na universal" />
          <h2 class="col-12 px-0">
            Nossos valores, visões e qualidades
          </h2>
        </div>
        <p class="p-title mt-3 mt-md-0">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias architecto magni
          impedit rem facere ex soluta ipsum aut. Neque, quae? Earum aliquid placeat.
        </p>
      </div>
      <div class="col-5 d-none d-lg-block px-0 img_valores">
        <img src="../assets/img/valores.webp" class="img-fluid shadow border" alt="">
      </div>
      <div class="col-lg-5 px-0 mae_swiper" @mouseenter="stopSlide" @mouseleave="runSlide">
        <swiper
          id="swiper-valores"
          ref="swiperValores"
          class="swiper p-2"
          :options="swiperOption"
        >
          <swiper-slide
            v-for="swipers in items"
            :key="swipers.title"
            class="shadow-sm"
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
    </div>
  </section>
</template>
<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
import Badge from './parts/Badge.vue'
export default {
  components: {
    Swiper,
    SwiperSlide,
    Badge
  },
  data () {
    return {
      swiperOption: {
        direction: 'vertical',
        slidesPerView: 'auto',
        spaceBetween: 35,
        grabCursor: true,
        autoplay: {
          delay: 1500,
          disableOnInteraction: false
        }
      },
      items: [
        {
          title: 'Investigação empresarial',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'cash-outline'
        },
        {
          title: 'Investigação conjugal',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'cash-outline'
        },
        {
          title: 'Investigação política',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'cash-outline'
        },
        {
          title: 'Localização de pessoas',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laborum, soluta eligendi',
          icon: 'cash-outline'
        }
      ]
    }
  },
  methods: {
    stopSlide () {
      this.$refs.swiperValores.$swiper.autoplay.stop()
    },
    runSlide () {
      this.$refs.swiperValores.$swiper.autoplay.start()
    }
  }
}
</script>
<style lang="scss" scoped>
  .container{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;

    .p-title{
      max-width: 500px;
      margin-bottom: 0 !important;
    }

    .titulo_functions{
      max-width: 380px;
    }

    .img_valores{
      img{
        height: 100%;
        width: 100%;
        object-fit: cover;
        border-radius: 45px 0 45px 0;
      }
    }

    .mae_swiper{
      .swiper{
        height: 630px;

        @media (max-width: 992px) {
          &{
            height: 60vh !important;
          }
        }

        .swiper-slide{
          background-color: white;
          padding: 20px 30px;
          box-shadow: 0 0.1rem 0.7rem rgba(0, 0, 0, 0.179) !important;
          border-radius: 35px 0 35px 0;
          color: var(--grafite);
          width: 100%;

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

        .swiper-slide:nth-child(even){
          background-color: var(--azul);
          color: var(--white);

          .circulo_icon{
            background-color: var(--azul_super_escuro);
          }
        }
      }
    }
  }
</style>
