<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Investigação empresarial"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/investigacao-empresarial.webp')"
        title-badge="atividades ilícitas"
        parte-azul="Serviços:"
        title-header="Investigação empresarial"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Existem graves acontecimentos de ordem administrativa e laboral com que por vezes as empresas se
        deparam. Fatores determinantes de origem interna ou externa, colidem com os interesses econômicos,
        jurídicos e sociais da empresa."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          O que preciso saber?
        </h2>
        <p>
          A investigação privada, assume um papel importante no auxílio a empresas e gestores, atuando em diferentes áreas.
          <br>
          <br>
          Existem graves acontecimentos de ordem administrativa e laboral com que por vezes as empresas se deparam. Fatores determinantes de origem interna ou externa, colidem com os interesses econômicos, jurídicos e sociais da empresa.
          <br>
          <br>
          Tais acontecimentos provêm inúmeras vezes da existência de concorrência desleal e fugas de informação.
        </p>
        <h2 class="azul mb-3">
          Preciso mesmo de uma investigação empresarial?
        </h2>
        <p>
          Poderão ser desenvolvidas investigações centradas nos seguintes tópicos:
        </p>
        <ul class="p-0 pl-4">
          <li>
            Informação e investigação de sociedades comerciais e industriais;
          </li>
          <li>
            Investigação de gestores;
          </li>
          <li>
            Concorrência Desleal;
          </li>
          <li>
            Averiguação de condutas duvidosas;
          </li>
          <li>
            Investigação e Informação para contratação e seleção de pessoal;
          </li>
          <li>
            Antecedentes Profissionais;
          </li>
          <li>
            Pesquisa e documentação;
          </li>
          <li>
            Inquéritos;
          </li>
          <li>
            Dentre outros;
          </li>
        </ul>
        <p>
          Para mais informações, não hesite em entrar em contato conosco hoje mesmo que teremos satisfação em lhe auxiliar
          da melhor forma possível.
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
    title: 'Investigação empresarial :: Universal Detetives'
  }
}
</script>
<style lang="scss" scoped>

</style>
