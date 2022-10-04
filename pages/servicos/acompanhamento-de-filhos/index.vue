<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Acompanhamento de filhos"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/acompanhamento-de-filhos.webp')"
        title-badge="más companhias"
        parte-azul="Serviços:"
        title-header="Acompanhamento de filhos"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Os seus filhos já não se contentam em ficar debaixo da sua vista, querem sair à noite com os
        amigos, é normal. No entanto é necessário prevenir excessos..."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          O que preciso saber?
        </h2>
        <p>
          Os seus filhos já não se contentam em ficar debaixo da sua vista, querem sair à noite com os amigos, é normal. No entanto é necessário prevenir excessos...
        </p>
        <p>
          Os sinais de comportamento desviante nos jovens alertam para que sejam redobradas as atenções numa fase que se pode revelar complicada para uma família.
        </p>
        <p>
          Como sabemos, por vezes a irreverência dos jovens compromete qualquer tentativa de abordagem por parte dos pais, que se esforçam por entender as bruscas mudanças de comportamento, temendo que muitas das vezes o jovem envergue pelo caminho da delinquência e do crime, e do consumo de drogas e entorpecentes.
        </p>
        <p>
          Uma investigação deste género servirá para que os pais percebam em que tipo de atividades o jovem estará envolvido, em que meio se encontra inserido, e quais as pessoas que o rodeiam.
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
    title: 'Acompanhamento de filhos :: Universal Detectives'
  }
}
</script>
<style lang="scss" scoped>

</style>
