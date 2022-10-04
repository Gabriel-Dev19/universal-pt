<template>
  <section>
    <div class="container">
      <div class="row mx-0">
        <Badge name="soluções" />
        <h2 class="col-12 px-0 mb-0">
          Revelamos a verdade!
        </h2>
      </div>
      <div class="mae_cards">
        <div v-for="item in cars_solutions" :key="item.title" class="cards_solutions shadow">
          <div class="mae_icon">
            <div class="circulo-alvo" />
            <div class="seta-vertical-alvo" />
            <div class="seta-horizontal-alvo" />
            <ion-icon :name="item.icon" />
          </div>
          <h6>
            {{ item.title }}
          </h6>
          <p>
            {{ item.description }}
          </p>
        </div>
      </div>
      <div class="mae_numeros mt-5">
        <div v-for="item in numeros" :key="item.numero" class="numeros shadow">
          <div class="icon">
            <ion-icon :name="item.icon" />
          </div>
          <div class="quadradro_branco">
            <h2>
              {{ item.numero }}{{ item.porcent }}
            </h2>
            <span>
              {{ item.description }}
            </span>
          </div>
        </div>
      </div>
      <div class="d-flex mt-5 pt-4 justify-content-center">
        <ButtonScrollContato name="Entre em contacto com nossa equipa" variation="seta" />
      </div>
    </div>
  </section>
</template>
<script>
import ButtonScrollContato from './buttons/button-scroll-contato.vue'
import Badge from './parts/Badge.vue'
export default {
  components: { Badge, ButtonScrollContato },
  data () {
    return {
      cars_solutions: [
        {
          icon: 'finger-print',
          title: 'Missão',
          description: `Entregar resultados exatos e proporcionar mais segurança aos nossos clientes, por meio
          da atuação especializada e do fornecimento de serviços de qualidade e excelência em investigação.`
        },
        {
          icon: 'eye-outline',
          title: 'Visão',
          description: `Ser reconhecida pelos clientes como referência nacional no ramo de investigação,
          por meio da ética, do compromisso e do profissionalismo.`
        },
        {
          icon: 'trophy-outline',
          title: 'Valores',
          description: `Ética, compromisso e profissionalismo - esses são os três pilares que norteiam nossas
          atividades. Tudo para oferecer aos nossos clientes produtos, serviços e parcerias de excelência no que fazemos.`
        }
      ],
      numeros: [
        {
          numero: 302,
          description: 'clientes satisfeitos',
          icon: 'happy-outline'
        },
        {
          numero: 670,
          description: 'xícaras de café',
          icon: 'cafe-outline'
        },
        {
          numero: 57,
          description: 'detectives credenciados',
          icon: 'medal-outline'
        },
        {
          numero: 100,
          porcent: '%',
          description: 'dos casos resolvidos',
          icon: 'trophy-outline'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
section{
  padding: 80px 0;
  margin-top: 150px;
  background-color: var(--cinza_super_claro);

  .mae_cards{
    display: flex;
    flex-wrap: wrap;

    .cards_solutions{
      background-color: white;
      margin-top: 50px;
      width: 100%;
      padding: 30px;
      border-radius: 20px;

      .mae_icon{
        position: relative;
        height: 65px;
        width: 65px;
        display: flex;
        justify-content: center;
        align-items: center;

        .circulo-alvo{
          position: absolute;
          width: 100%;
          height: 100%;
          border-radius: 50%;
          border: 3px solid var(--grafite);
        }
        .seta-vertical-alvo{
          height: 100%;
          width: 3px;
          position: absolute;
          background-color: var(--grafite);
          top: 0;
        }
        .seta-horizontal-alvo{
          width: 100%;
          height: 3px;
          position: absolute;
          background-color: var(--grafite);
          left: 0;
        }

        ion-icon{
          position: absolute;
          font-size: 40px;
          min-width: 40px;
          color: var(--azul_escuro);
          background-color: white;
          border-radius: 15px;
          padding: 3px;
        }
      }

      h6{
        font-weight: 700;
        margin-top: 30px;
      }

      p{
        margin-top: 20px;
        font-size: 15px;
        margin-bottom: 0 !important;
      }

      @media (min-width: 992px) {
        flex-basis: 0;
        flex-grow: 1;
        max-width: 100%;
        width: auto;

        &:nth-child(3n+2){
          margin-left: 50px;
          margin-right: 50px;
        }
      }
    }
  }

  .mae_numeros{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;

    .numeros{
      padding-top: 7px;
      padding-left: 7px;
      margin-top: 50px;
      background-color: var(--azul_escuro);
      border-radius: 30px 30px 0 30px;

      .icon{
        width: 50px;
        height: 50px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: var(--white);

        ion-icon{
          min-width: 35px;
          font-size: 35px;
          color: var(--dark);
          --ionicon-stroke-width: 25px;
        }
      }

      .quadradro_branco{
        margin-left: 45px;
        margin-top: 5px;
        border-radius: 30px 30px 0 30px;
        background-color: white;
        padding: 50px 25px 25px 25px;

        h2{
          font-size: 50px;
          font-weight: 300;
          line-height: 0;
        }

        span{
          display: block;
          margin-top: 40px;
          width: 125px;
          text-transform: uppercase;
          font-size: 15px;
        }
      }

      @media (max-width: 575.95px) {
        &{
          width: 100%;
          max-width: 280px;
        }
      }

      @media (min-width: 576px) and (max-width: 1200px) {
        &{
          width: 45%;
        }
      }
    }

    @media (max-width: 575.95px) {
      &{
        justify-content: center;
      }
    }

    @media (min-width: 576px) and (max-width: 1200px) {
      &{
        justify-content: space-between;
      }
    }

  }
}
</style>
