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
    </div>
  </section>
</template>
<script>
import Badge from './parts/Badge.vue'
export default {
  components: { Badge },
  data () {
    return {
      cars_solutions: [
        {
          icon: 'finger-print',
          title: 'Registro de provas e documentação completa',
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, libero iste nesciunt
            ipsum dolor sit am adipisicing elit. Facilis, libero iste nesciunt`
        },
        {
          icon: 'finger-print',
          title: 'Registro de provas e documentação completa',
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, libero iste nesciunt
            ipsum dolor sit am adipisicing elit. Facilis, libero iste nesciunt`
        },
        {
          icon: 'finger-print',
          title: 'Registro de provas e documentação completa',
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, libero iste nesciunt
            ipsum dolor sit am adipisicing elit. Facilis, libero iste nesciunt`
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
}
</style>
