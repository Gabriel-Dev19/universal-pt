<template>
  <section id="servicos">
    <div class="container">
      <HeaderSections
        style="margin-top: 200px"
        :is-reverse="true"
        :img="require('../assets/img/detetive-lupa.webp')"
        title-badge="serviços"
        parte-azul="Nossos serviços"
        title-header="de investigação privada"
        subtitle="Realizamos todos os tipos de serviços de investigação privada"
        description="Conheça os nossos serviços de investigação direcionados para particulares e empresas.
        Averiguamos todo o tipo de situações dentro do âmbito privado, resolvemos os mais variados
        assuntos, tais como problemas com filhos menores, casos conjugais, setor industrial, comercial,
        provas para advogados e muito mais. Consulte-nos!"
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
            <div class="d-flex">
              <nuxt-link :to="items.routerTo" class="link-seta mt-4">
                {{ items.linkTitle }}
                <div class="mae_seta">
                  <div class="seta">
                    <ion-icon name="chevron-forward-outline" />
                  </div>
                </div>
              </nuxt-link>
            </div>
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
          description: `Existem graves acontecimentos de ordem administrativa e laboral com que por vezes as empresas
          se deparam. Fatores determinantes
          de origem interna ou externa, colidem com os interesses econômicos, jurídicos e sociais da empresa.`,
          linkTitle: 'Investigação empresarial',
          routerTo: '/servicos/investigacao-empresarial'
        },
        {
          img: require('../assets/img/servicos/investigacao-conjugal.webp'),
          altImg: 'Investigação conjugal',
          badge: 'Infidelidade e traição',
          title: 'Investigação conjugal',
          description: `Quando os ciúmes e as desconfianças de traição, brigas e discussões sobre a infidelidade
          do cônjuge são frequentes na vida do casal, pode ter certeza que é a hora de contratar um profissional
          de investigação privada para tentar descobrir a verdade e acalmar seus ânimos afim de ter sua tão
          sonhada paz novamente.`,
          linkTitle: 'Investigação conjugal',
          routerTo: '/servicos/investigacao-conjugal'
        },
        {
          img: require('../assets/img/servicos/investigacao-politica.webp'),
          altImg: 'Investigação politica',
          badge: 'Eleições fraudulentas',
          title: 'Investigação politica',
          description: `A equipa da Universal Detectives está apta a resolver desde os simples até os mais complexos casos
          de investigação pública e política. Sempre mantendo o foco, nossos agentes recebem treinamentos para
          estarem sempre bem informados, e assim, poderem chegar ao melhor resultado final desejado pelo cliente
          com fatos e dados evidenciados.`,
          linkTitle: 'Investigação politica',
          routerTo: '/servicos/investigacao-politica'
        },
        {
          img: require('../assets/img/servicos/localizacao-de-pessoas.webp'),
          altImg: 'Localizacao de pessoas',
          badge: 'Pessoas desaparecidas',
          title: 'Localizacao de pessoas',
          description: `Localizamos pessoas desaparecidas, familiares e amigos que o tempo se encarregou de afastar
          ou que eventualmente possam ter deixado de dar notícias, voluntária ou involuntariamente.`,
          linkTitle: 'Localizacao de pessoas',
          routerTo: '/servicos/localizacao-de-pessoas'
        },
        {
          img: require('../assets/img/servicos/acompanhamento-de-filhos.webp'),
          altImg: 'Acompanhamento de filhos',
          badge: 'Filhos rebeldes',
          title: 'Acompanhamento de filhos',
          description: `Como sabemos, por vezes a irreverência dos jovens compromete qualquer tentativa de abordagem
          por parte dos pais, que se esforçam por entender as bruscas mudanças de comportamento, temendo
          que muitas das vezes o jovem envergue pelo caminho da delinquência e do crime, e do consumo de
          drogas e entorpecentes.`,
          linkTitle: 'Acompanhamento de filhos',
          routerTo: '/servicos/acompanhamento-de-filhos'
        },
        {
          img: require('../assets/img/servicos/celular-vip.webp'),
          altImg: 'Telemóvel VIP',
          badge: 'Telemóvel VIP',
          title: 'Telemóvel VIP',
          description: `Telemóvel VIP é um incrível aplicativo de monitoramento móvel! Através dele você poderá gravar tudo,
          desde o histórico de chamadas, mensagens de texto, as palavras digitadas, mesmo as deletadas, em todos os apps,
          como Facebook e mais.`,
          linkTitle: 'Telemóvel VIP',
          routerTo: '/servicos/celular-VIP'
        },
        {
          img: require('../assets/img/servicos/curso-de-detetive.jpg'),
          altImg: 'Curso de detective privado universal detectives',
          badge: 'aprendizado',
          title: 'Curso de detective',
          description: `Venha se especializar com quem realmente entende do assunto. Realizando nosso Curso de Detective
          Privado da Universal Detectives, você estará recebendo online um material de qualidade para estudar em suas
          horas vagas, dentro do seu próprio ritmo.`,
          linkTitle: 'Curso de detective',
          routerTo: '/servicos/curso-de-detective-privado'
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
          display: -webkit-box;
          -webkit-line-clamp: 4;
          -webkit-box-orient: vertical;
          overflow: hidden;
          text-overflow: ellipsis;
          margin-bottom: 0 !important;
          font-size: 15px;
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
