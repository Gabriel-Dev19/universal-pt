<template>
  <section>
    <div class="container align-content-start align-items-start row mx-auto">
      <div class="row col-lg-4 px-0 mx-0">
        <Badge name="Dúvidas?" />
        <h2 class="col-12 px-0">
          Perguntas frequentes
        </h2>
        <p class="col-12 px-0 mb-0 mt-2">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam maxime eveniet quisquam doloribus,
          fugiat quod enim, provident dolores, ex iusto mollitia aut pariatur sapiente alias non tempora
          ut molestiae? Pariatur!
        </p>
        <div class="col-12 mt-4 px-0">
          <ButtonScrollContato name="Faça uma pergunta" variation="lg-azul" />
        </div>
        <div class="col-12 mt-4 pt-2 px-0">
          <ButtonScrollContato name="Contate nossa equipe" variation="seta" />
        </div>
      </div>
      <div class="mae_perguntas col-lg ml-lg-5 pl-lg-5 px-0">
        <div v-for="(item, index) in faqs" :key="item.question" class="faq">
          <button v-b-toggle="`faq-${index}`" class="question text-left btn px-0">
            <h6>{{ item.question }}</h6>
            <ion-icon class="ml-2" name="add-outline" />
            <ion-icon class="ml-2" name="remove-outline" />
          </button>
          <b-collapse :id="`faq-${index}`">
            <div class="response">
              {{ item.response }}
            </div>
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
          question: 'Alguma pergunt',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma pergun',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma pergu',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma perg',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma per',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma pe',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma perguntaa',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma perguntaaa',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
        },
        {
          question: 'Alguma perguntaaaa',
          response: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos illum suscipit
                  deleniti doloremque possimus aut esse sapiente numquam`
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
