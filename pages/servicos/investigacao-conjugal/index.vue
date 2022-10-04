<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Investigação conjugal"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/investigacao-conjugal.webp')"
        title-badge="matrimonial"
        parte-azul="Serviços:"
        title-header="Investigação conjugal"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Quando os ciúmes e as desconfianças de traição, brigas e discussões sobre a infidelidade
        do cônjuge são frequentes na vida do casal, pode ter certeza que é a hora de contratar um profissional
        de investigação privada."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          O que preciso saber?
        </h2>
        <p>
          Quando os ciúmes e as desconfianças de traição, brigas e discussões sobre a infidelidade do cônjuge são frequentes na vida do casal, pode ter certeza que é a hora de contratar um profissional de investigação privada para tentar descobrir a verdade e acalmar seus ânimos afim de ter sua tão sonhada paz novamente.
          <br>
          <br>
          A Universal Detectives conta com profissionais qualificados e altamente treinados para poder ajudar você a desvendar essa situação, não perca mais tempo entre em contacto conosco hoje mesmo.
        </p>
        <div class="row mx-0">
          <ButtonScrollContato name="Fale com um especialista" variation="lg-azul" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import ButtonScrollContato from '~/components/buttons/button-scroll-contato.vue'
import HeaderSections from '~/components/parts/HeaderSections.vue'

export default {
  components: { HeaderSections, ButtonScrollContato },
  layout: 'layoutSobre',
  head: {
    title: 'Investigação conjugal :: Universal Detectives'
  }
}
</script>
<style lang="scss" scoped>

</style>
