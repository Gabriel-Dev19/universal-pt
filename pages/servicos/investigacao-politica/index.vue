<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Investigação política"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/investigacao-politica.webp')"
        title-badge="eleições fraudulentas"
        parte-azul="Serviços:"
        title-header="Investigação política"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Atualmente na situação política do país, os políticos devem estar atentos pois
        tudo pode ser motivo para a perda de votos, ou mesmo desmascarar desavenças e concorrentes."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          O que preciso saber?
        </h2>
        <p>
          A Universal Detetives, conta com equipe especializada para investigações políticas e de políticos, com tecnologia e modelo de processo diferenciado para cada caso.
          <br>
          <br>
          Atualmente na situação política do país, os políticos devem estar atentos pois tudo pode ser motivo para a perda de votos, ou mesmo desmascarar desavenças e concorrentes.
          <br>
          <br>
          A equipe da Universal Detetives está apta a resolver desde os simples até os mais complexos casos de investigação pública e política.
          <br>
          <br>
          Sempre mantendo o foco, nossos agentes recebem treinamentos para estarem sempre bem informados, e assim, poderem chegar ao melhor resultado final desejado pelo cliente com fatos e dados evidenciados.
          <br>
          <br>
          Agindo sempre dentro da lei, portando todas as provas levantadas durante o período investigativo poderão ser usadas em um tribunal. Além de manter compromisso e agindo sempre com o sigilo absoluto.
          <br>
          <br>
          O diferencial da Universal Detetives, além de manter um arsenal de equipamentos de última geração contem uns dos maiores bancos de dados atualizados do país, o que torna nosso trabalho mais rápido e eficiente.
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
    title: 'Investigação política :: Universal Detetives'
  }
}
</script>
<style lang="scss" scoped>

</style>
