<template>
  <section>
    <div class="container">
      <div class="box_titulo_explore px-2">
        <h2>
          Explore nosso trabalho!
        </h2>
        <div>
          <button class="btn p-0 button-next">
            <ion-icon name="arrow-forward-circle-outline" />
          </button>
        </div>
      </div>
      <swiper id="swiper-explore" class="swiper p-2" :options="swiperOption">
        <swiper-slide v-for="swipers in slides" :key="swipers.title" class="shadow-sm">
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

export default {
  // eslint-disable-next-line vue/component-definition-name-casing
  name: 'swiper-example-grab-cursor',
  title: 'Grab cursor',
  components: {
    Swiper,
    SwiperSlide
  },
  data () {
    return {
      swiperOption: {
        slidesPerView: 'auto',
        spaceBetween: 35,
        grabCursor: true,
        navigation: {
          nextEl: '.button-next'
        }
      },
      slides: [
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        },
        {
          title: 'Investigação conjugal',
          description: 'Alguma coisa de algum tema qualquer de coisa',
          icon: 'heart-dislike'
        }
      ]
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
    align-items: center;

    h2{
      font-size: 35px;
      font-weight: 600;
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

    .swiper-slide{
      padding: 25px;
      border-radius: 20px;
      background-color: white;
      color: var(--grafite);
      width: 300px;

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
      }

      p{
        font-size: 14px;
        margin-bottom: 0 !important;
      }
    }
    .swiper-slide:nth-child(2){
      padding: 25px;
      border-radius: 20px;
      background-color: var(--azul);
      color: var(--white);
      width: 300px;

      .circulo_icon{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 48px;
        height: 48px;
        border-radius: 50%;
        background-color: var(--azul_super_escuro);

        ion-icon{
          font-size: 28px;
        }
      }

      h6{
        margin-top: 18px;
        font-weight: 600;
      }

      p{
        font-size: 14px;
        margin-bottom: 0 !important;
      }
    }
  }
</style>
