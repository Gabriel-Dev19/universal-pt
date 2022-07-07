<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Localização de pessoas"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/localizacao-de-pessoas.webp')"
        title-badge="pessoas desaparecidas"
        parte-azul="Serviços:"
        title-header="Localização de pessoas"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Localizamos pessoas desaparecidas, familiares e amigos que o tempo se encarregou de
        afastar ou que eventualmente possam ter deixado de dar notícias, voluntária ou involuntariamente."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          Localização de Pessoas desaparecidas, Familiares ou Amigos
        </h2>
        <p>
          Localizamos pessoas desaparecidas, familiares e amigos que o tempo se encarregou de afastar ou que eventualmente possam ter deixado de dar notícias, voluntária ou involuntariamente.
        </p>
        <h2 class="azul mb-3">
          Localização de Namorados
        </h2>
        <p>
          Aquele namorado ou namorada da adolescência não sai da sua cabeça? Aquele "flirt" de verão terminou, mas ficou a lembrança e a vontade do reencontro? Podemos contribuir para que volte a ser a ter um sorriso nos lábios! Entre em contato conosco agora mesmo que teremos a satisfação em lhe ajudar a desvendar essa situação.
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
    title: 'Localização de pessoas :: Universal Detetives'
  }
}
</script>
<style lang="scss" scoped>

</style>
