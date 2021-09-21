<template>
  <section>
    <div class="container">
      <HeaderSections :is-reverse="true" />
      <div class="mae_cards">
        <div v-for="items in cardsServices" :key="items.tile" class="cards">
          <div class="slot_img">
            <img :src="items.img" class="img-fluid" :alt="items.altImg">
          </div>
          <div class="card_service_body">
            <div class="detalhe-azul">
              <div class="traco" /> {{ items.badge }}
            </div>
            <h5>
              {{ items.title }}
            </h5>
            <p>
              {{ items.description }}
            </p>
            <nuxt-link :to="items.routerTo" class="nuxt-link-servicos">
              {{ items.linkTitle }}
              <div class="circulo-azul">
                <ion-icon name="chevron-forward-outline" />
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import HeaderSections from './parts/HeaderSections.vue'

export default {
  components: { HeaderSections },
  data () {
    return {
      cardsServices: [
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/detetive-lupa.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          icon: 'cash-outline',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
  .mae_cards{
    margin-top: 100px;
    display: flex;
    flex-wrap: wrap;

    @media (min-width: 768px) {
      &{
        margin-top: 200px !important;
      }
    }

    .cards{
      border-radius: 20px;
      box-shadow: 0 0.1rem 0.7rem rgba(0, 0, 0, 0.274) !important;
      overflow: hidden;
      padding-bottom: 25px;
      margin-top: 40px;

      .slot_img{
        height: 250px;
        width: 100%;

        img{
          height: 100%;
          width: 100%;
          object-fit: cover;
        }
      }

      .card_service_body{
        padding: 0 25px;
        margin-top: 20px;

        .detalhe-azul{
          display: flex;
          align-items: center;
          color: var(--azul_escuro);
          font-weight: 500;
          letter-spacing: 0.3px;
          font-size: 15px;

          .traco{
            width: 40px;
            height: 1px;
            margin-right: 10px;
            background-color: var(--azul);
          }
        }

        h5{
          margin-top: 15px;
          font-weight: 600;
          letter-spacing: 0.3px;
        }

        p{
          margin-bottom: 0 !important;
          font-size: 15px;
        }

        .nuxt-link-servicos{
          display: flex;
          align-items: center;
          margin-top: 25px;
          color: var(--azul_escuro) !important;
          font-weight: 600;
          letter-spacing: 0.3px;
          font-size: 17px;

          &:hover{
            text-decoration: underline;
          }

          .circulo-azul{
            min-height: 25px;
            min-width: 25px;
            border-radius: 50%;
            background-color: var(--azul_escuro);
            color: white;
            margin-left: 10px;
            display: flex;
            justify-content: center;
            align-items: center;

            ion-icon{
              font-size: 16px;
              min-width: 16px;
              margin-bottom: 1px;
              margin-left: 1px;
            }
          }
        }
      }

      @media (min-width: 768px) and (max-width: 1199.95px) {
        &{
          margin-top: 6%;
          width: 47%;
        }

        &:nth-child(2n+1){
          margin-right: 6%;
        }
      }

      @media (min-width: 1200px) {
        &{
          margin-top: 3.5%;
          width: 31%;
        }

        &:nth-child(3n+2){
          margin-left: 3.5%;
          margin-right: 3.5%;
        }
      }
    }
  }
</style>
