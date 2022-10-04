<template>
  <section>
    <div class="container align-content-start align-items-start row mx-auto">
      <div class="row col-lg-4 px-0 mx-0">
        <Badge name="Dúvidas?" />
        <h2 class="col-12 px-0">
          Perguntas frequentes
        </h2>
        <p class="col-12 px-0 mb-0 mt-2">
          A profissão do detective privado é completamente rodeada de mistérios. Consequentemente, é normal
          que surjam diversas perguntas relacionadas ao dia a
          dia desses profissionais e às agências de detectives. Afinal, existem muitos equívocos comuns
          sobre o que ou como um investigador realmente é.
        </p>
        <div class="col-12 mt-4 px-0">
          <ButtonScrollContato name="Faça uma pergunta" variation="lg-azul" />
        </div>
        <div class="col-12 mt-4 pt-2 px-0">
          <ButtonScrollContato name="Contate nossa equipa" variation="seta" />
        </div>
      </div>
      <div class="mae_perguntas col-lg ml-lg-5 pl-lg-5 px-0">
        <div v-for="(item, index) in faqs" :key="item.question" class="faq">
          <button v-b-toggle="`faq-${index}`" class="question text-left btn px-0">
            <h6 v-html="item.question" />
            <ion-icon class="ml-2" name="add-outline" />
            <ion-icon class="ml-2" name="remove-outline" />
          </button>
          <b-collapse :id="`faq-${index}`">
            <div class="response" v-html="item.response" />
          </b-collapse>
        </div>
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
      faqs: [
        {
          question: 'O que faz um <br> detective privado?',
          response: `Na ficção, o detective normalmente é um sujeito rodeado de mistérios
          que ajuda a polícia a desvendar crimes e, por consequência, vive muitas situações de perigo.
          Um detective privado, na realidade, é um profissional capacitado para conduzir uma investigação, a fim
          de descobrir certas informações e coletar as evidências pertinentes para cada cliente. Na vida real,
          portanto, ele pode trabalhar em diversos tipos de casos, inclusive que não sejam criminais.
          <br>
          <br>
          Existem várias tarefas que fazem parte do escopo de atividades de um detective privado, sobretudo porque
          existe uma variedade de serviços que são oferecidos para os seus clientes. Isso envolve fazer pesquisas
          online, entrevistar pessoas, ficar de campana, seguir o investigado, se infiltrar nos lugares e etc.
          `
        },
        {
          question: 'Quais são os tipos de investigações realizadas por um detective privado?',
          response: `O detective privado pode realizar diversos tipos de investigação, como casos de
          direito de família, incluindo custódia dos filhos, divórcio e de pensão alimentícia. Eles também
          podem ser contratados para ajudar a localizar ativos, localizar documentos ou fazer verificações
          de antecedentes. Obviamente esses são apenas alguns exemplos do campo de atuação desse profissional.
          <br>
          <br>
          De forma geral, entre as possibilidades de atuação de um detective privado, podem ser destacadas:
          <br>
          <br>
          <ul class="p-0 pl-4">
            <li>
              Investigação conjugal;
            </li>
            <li>
              Investigação empresarial;
            </li>
            <li>
              Investigação familiar;
            </li>
            <li>
              Contrainteligência;
            </li>
            <li>
              Monitoramento;
            </li>
            <li>
              Localização de pessoas;
            </li>
          </ul>
          `
        },
        {
          question: 'Quanto custa para contratar um detective privado?',
          response: `Essa pergunta não tem uma resposta exata. Isso porque os custos da
          investigação dependem de diversos fatores, como por exemplo o tipo de investigação, o tempo que
          vai durar todo o processo investigativo, a quantidade de profissionais envolvidos e etc. Mas, em
          média, os custos são:
          <br>
          <br>
          <ul class="p-0 pl-4">
            <li>
              Investigação conjugal –  1.000 € a  5.000 €;
            </li>
            <li>
              Investigação empresarial –  5.000 € a  20.000 €;
            </li>
            <li>
              Investigação familiar –  1.000 € a  5.000 €;
            </li>
            <li>
              Contra inteligência –  2.000 € a  10.000 €;
            </li>
            <li>
              Localização de pessoas –  2.000 € a  10.000 €;
            </li>
            <li>
              Monitoramento –  1.000 € a  1.200 € (diária);
            </li>
            <li>
              Investigação privado –  1.000 € a  5.000 €.
            </li>
          </ul>
          <br>
          <br>
          É válido ressaltar mais uma vez, no entanto, que como cada caso possui as suas particularidades,
          o custo pode ser bastante variável. Essas médias citadas acima, portanto, não fazem parte de uma
          tabela de preços oficial, podendo os valores serem diferentes na hora da contratação.
          `
        },
        {
          question: 'Quanto tempo dura <br> uma investigação?',
          response: `Outra pergunta que não tem uma resposta exata, pois o tempo que dura uma investigação
          depende da complexidade de cada caso. Se o investigado for uma pessoa mais reservada, por exemplo, pode
          levar mais tempo para o detective privado poder reunir as informações necessárias e coletar as provas
          que precisa. Contudo, também existem algumas estimativas. Mas, novamente, são apenas uma média:
          <br>
          <br>
          <ul class="p-0 pl-4">
            <li>
              Investigação conjugal e familiar de 05 a 10 dias;
            </li>
            <li>
              Investigação empresarial de 05 a 90 dias;
            </li>
          </ul>
          `
        },
        {
          question: 'A pessoa investigada pode acabar descobrindo sobre a investigação?',
          response: `O detective privado deve atuar seguindo o código de ética da profissão, mantendo o máximo sigilo
          e discrição durante o andamento dos processos investigativos. Obviamente, existem sim riscos da pessoa investigada
          descobrir sobre a investigação. Principalmente porque o próprio cliente pode acabar deixando escapar essa informação
          por conta da ansiedade que é gerada ao longo do trabalho. Por isso, é muito importante saber controlar as próprias
          emoções e manter o comportamento normal durante o período de investigações.
          <br>
          <br>
          Alguns cuidados ainda são recomendados, como mudar as senhas de todos os dispositivos e contas de e-mail. Ou até
          mesmo criar um e-mail novo somente para receber o material do resultado das investigações. O sigilo por parte do
          cliente também é importante, sobretudo se tiver amigos em comum com a pessoa investigada.
          <br>
          <br>
          Mas, de qualquer forma, o detective tem o treinamento adequado para essas situações. Todos os procedimentos são
          informados ao cliente no ato da contratação. Por exemplo, se for percebido que existe a chance da pessoa descobrir,
          o trabalho será abortado no momento. Dessa forma, garantindo a continuidade da investigação posteriormente.
          `
        },
        {
          question: 'Como e quais são as provas coletadas pelo detective privado?',
          response: `Para ajudá-lo a conduzir as investigações, o detective privado pode contar com a ajuda de diversos
          equipamentos tecnológicos, tais como câmeras, escutas e rastreadores. Dessa forma, é possível coletar vários
          tipos de provas durante uma investigação privada. Como, por exemplo, fotos, vídeos, áudios, localizações e etc.`
        },
        {
          question: 'As provas podem ser usadas em processos judiciais?',
          response: `Sim, as evidências coletadas pelo detective privado podem ser usadas como provas em processos
          judiciais! Contudo, é necessário que tanto o profissional quanto o cliente tenha auxílio jurídico para tal.
          E cabe ao detective seguir o código de ética da profissão e agir em conformidade com as leis vigentes, prezando
          sempre pela legitimidade e legalidade das provas obtidas ao longo do processo investigativo.`
        },
        {
          question: 'Quais os diferenciais nos serviços prestados pela Universal Detectives?',
          response: `A Universal Detectives é uma empresa que está há mais de 20 anos atuando na área de investigação
          privado, oferecendo diversos tipos de investigação. Nossos diferenciais incluem uma equipa de detectives
          particulares altamente qualificados, transparência em todo o processo, qualidade do material apresentado,
          procedimentos de segurança para preservar o sigilo do nosso cliente e grande retorno aos mesmos.`
        }
      ]
    }
  }

}
</script>
<style lang="scss" scoped>
  section{
    padding: 80px 0;
    background-color: var(--cinza_super_claro);

    .mae_perguntas{
      display: flex;
      flex-wrap: wrap;
      align-items: flex-start;

      .faq{
        margin-top: 55px;
        width: 100%;
        border-bottom: 1px solid #c0c0c0;
        padding-bottom: 5px;

        @media (min-width: 768px) {
          &{
            width: 47%;
          }
          &:nth-child(2n+1){
            margin-right: 6%;
          }
        }

        @media (min-width: 992px) {
          &:nth-child(1), &:nth-child(2){
            margin-top: 0 !important;
          }
        }

        .question{
          display: flex;
          justify-content: space-between;
          align-items: center;
          width: 100%;

          h6{
            font-weight: 700;
            margin-bottom: 0 !important;
          }

          ion-icon{
            font-size: 22px;
            min-width: 22px;
          }

          &[aria-expanded="true"]{
            ion-icon[name="add-outline"]{
              display: none;
            }
          }
          &[aria-expanded="false"]{
            ion-icon[name="remove-outline"]{
              display: none;
            }
          }
        }

        .response{
          margin-top: 10px;
          margin-bottom: 5px;
          font-size: 15px;
        }
      }
    }
  }
</style>
