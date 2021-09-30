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
        title-badge="adultério"
        parte-azul="Serviços:"
        title-header="Investigação conjugal"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum omnis
        aliquid perspiciatis quos, sequi ratione sunt possimus corrupti velit porro? Nobis
        ipsa dicta quasi repellendus, ducimus et deleniti tenetur delectus?"
      />
      <div class="container-text">
        <h2 class="azul mb-3">
          Como a universal trabalha?
        </h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
        </p>
        <h2 class="azul mb-3">
          Algum outro tema?
        </h2>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Ex nostrum quam tempora, cupiditate possimus in reprehenderit
          rem recusandae doloremque, officiis assumenda. Officiis eius sequi perspiciatis
          vero non expedita et aperiam?
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
  layout: 'layoutSobre'
}
</script>
<style lang="scss" scoped>

</style>
