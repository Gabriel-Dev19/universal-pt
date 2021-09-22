<template>
  <section>
    <div class="container">
      <HeaderSections
        :is-reverse="true"
        title-badge="serviços"
        parte-azul="Nossos serviços"
        title-header="de investigação particular"
        subtitle="Realizamos todos os tipos de serviços de investigação particular"
        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur
          quam voluptatem at porro commodi excepturi consectetur impedit animi, eum ratione saepe,
          magni aliquam ad? Voluptatibus assumenda voluptatem voluptas dolores amet!"
      />
      <div class="mae_cards">
        <div v-for="items in cardsServices" :key="items.tile" class="cards border">
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
              <div class="seta">
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
          img: require('../assets/img/servicos/investigacao-empresarial.webp'),
          altImg: 'Investigação empresarial',
          badge: 'Aividades ilícitas',
          title: 'Investigação empresarial',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação empresarial',
          routerTo: '/investigacao-empresarial'
        },
        {
          img: require('../assets/img/servicos/investigacao-conjugal.webp'),
          altImg: 'Investigação conjugal',
          badge: 'Infidelidade e traição',
          title: 'Investigação conjugal',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação conjugal',
          routerTo: '/investigacao-conjugal'
        },
        {
          img: require('../assets/img/servicos/investigacao-politica.webp'),
          altImg: 'Investigação politica',
          badge: 'Eleições fraudulentas',
          title: 'Investigação politica',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Investigação politica',
          routerTo: '/investigacao-politica'
        },
        {
          img: require('../assets/img/servicos/localizacao-de-pessoas.webp'),
          altImg: 'Localizacao de pessoas',
          badge: 'Pessoas desaparecidas',
          title: 'Localizacao de pessoas',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Localizacao de pessoas',
          routerTo: '/localizacao-de-pessoas'
        },
        {
          img: require('../assets/img/servicos/acompanhamento-de-filhos.webp'),
          altImg: 'Acompanhamento de filhos',
          badge: 'Filhos rebeldes',
          title: 'Acompanhamento de filhos',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Acompanhamento de filhos',
          routerTo: '/acompanhamento-de-filhos'
        },
        {
          img: require('../assets/img/servicos/celular-vip.webp'),
          altImg: 'Celular VIP',
          badge: 'Celular VIP',
          title: 'Celular VIP',
          description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vitae fuga nemo eum quis cumque dignissimos repellat fugit recusandae maxime tempore velit, exercitationem sequi',
          linkTitle: 'Celular VIP',
          routerTo: '/celular-VIP'
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
      box-shadow: 0 0.1rem 0.7rem rgba(0, 0, 0, 0.35) !important;
      overflow: hidden;
      padding-bottom: 25px;
      margin-top: 40px;
      transition: all .2s;

      &:hover{
        transform: scale3d(1.03, 1.03, 1.03);
      }

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
            text-decoration: none;

            .seta{
              width: 40px;
            }
          }

          .seta{
            position: relative;
            display: flex;
            align-items: center;
            width: 25px;
            height: 1px;
            color: var(--azul_escuro);
            margin-left: 15px;
            transition: all .3s;
            background-color: var(--azul_escuro);

            ion-icon{
              position: absolute;
              right: -10px;
              font-size: 15px;
              min-width: 15px;
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
