<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Curso de detetive particular"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/curso-de-detetive.jpg')"
        title-badge="aprendizado"
        parte-azul="Serviços:"
        title-header="Curso de detetive particular"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Venha se especializar com quem realmente entende do assunto. Realizando nosso Curso de Detetive
          Particular da Universal Detetives, você estará recebendo online um material de qualidade para estudar em suas
          horas vagas, dentro do seu próprio ritmo."
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          O que preciso saber?
        </h2>
        <p>
          Venha aprender com quem é especialista no ramo de Investigação Particular. Realizando
          nosso Curso de Detetive Particular, você estará recebendo conhecimento dos melhores detetives
          do Brasil e material de qualidade
          para estudar em suas horas vagas, no conforto da sua casa e tudo dentro do seu próprio tempo.
        </p>
        <h3 class="azul mb-3">
          Apostila de estudos:
        </h3>
        <p>
          Nossa apostila foi baseada em conhecimento adquirido em mais de 28 anos de atuação
          no ramo da investigação particular e redigida pelos profissionais mais experientes.
          Preparamos para você um material simples e
          objetivo, para você tirar todas as suas dúvidas e saber como se tornar um
          detetive particular de renome.
        </p>
        <h3 class="azul mb-3">
          Certificação:
        </h3>
        <p>
          Após conclusão do curso, você receberá o certificado de Detetive Particular
          impresso e autenticado por nossa empresa. Nosso certificado é a prova da sua procedência como detetive
          particular.
        </p>
        <h3 class="azul mb-3">
          Carteira de detetive particular:
        </h3>
        <p>
          Ao concluir o curso, além do certificado, você receberá também a Carteira e Porta Documentos
          de Detetive Particular Profissional.
        </p>
        <h2 class="azul mb-3">
          Adquira nosso curso:
        </h2>
        <h3 class="azul mb-3">
          Versão online:
        </h3>
        <p>
          <b>Enviaremos esta versão para seu E-mail</b> assim que o pagamento for concluído. Desta forma
          você terá em suas mãos o melhor conteúdo de investigação particular para estudar no celular, no tablet ou no PC
          de acordo com sua disponibilidade.
        </p>
        <button class="btn-azul-lg shadow mt-2 btn" @click="$root.$emit('ShowWhatsRemote')">
          Compre a versão online por R$ 989,90
        </button>
        <h3 class="azul mb-3">
          Versão impressa:
        </h3>
        <p>
          Enviaremos para sua casa o material didático, impresso em <b>papel colchê 180grs</b>, com acabamento
          de primeira linha e você terá em suas mãos a melhor apostila sobre Detetive Particular para
          estudar no seu tempo livre.
        </p>
        <button class="btn-azul-lg shadow mt-2 btn" @click="$root.$emit('ShowWhatsRemote')">
          Compre a versão impressa por R$ 1189,90
        </button>
        <div class="row mt-5 mx-0">
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
  layout: 'layoutSobre'
}
</script>
<style lang="scss" scoped>

</style>
