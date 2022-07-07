<template>
  <section>
    <Home
      name-btn="saiba mais"
      hash-btn="sobre"
      title-principal="Celular VIP"
    />
    <div id="sobre" class="container">
      <HeaderSections
        style="margin-top: 150px"
        :is-reverse="true"
        :img="require('../../../assets/img/servicos/celular-vip.webp')"
        title-badge="filhos menores"
        parte-azul="Serviços:"
        title-header="Celular VIP"
        subtitle="Somos uma agência comprometida com a excelência e a dedicação"
        description="Saiba TUDO o que seu filho faz no celular em apenas alguns minutos com o aplicativo
        fácil de instalar do CELULAR VIP, a maneira mais fácil de supervisionar todas as atividades do
        telefone do seu filho*"
      />
      <div class="container-text celular-vip-text">
        <h2 class="azul mb-3">
          Com Celular VIP, nunca foi tão fácil ser pai na era digital
        </h2>
        <p>
          Celular VIP é um incrível aplicativo de monitoramento móvel! Através dele você poderá gravar tudo,
          desde o histórico de chamadas, mensagens de texto, as palavras digitadas, mesmo as deletadas, em todos
          os apps, como Facebook e mais. Este produto é feito para monitorar seu filho* 24 horas de forma fácil.
          Você não vai perder nada. Você tem acesso a um painel de controle online exclusivo, apoio ao cliente e
          uma das melhores soluções de monitoramento móvel para proteger seu filho* contra danos, cyberbullying,
          predadores infantis e atitudes ruins que podem persegui-lo por anos.
        </p>
        <ul>
          <li>
            <ion-icon name="phone-portrait-outline" />
            <p>
              Registramos todos os números de telefone discados, todas as ligações (número de telefone) recebidas e todas as
              ligações perdidas.
            </p>
          </li>
          <li>
            <ion-icon name="location-outline" />
            <p>
              Veja a localização atual do smartphone do seu filho, bem como o local do histórico do telefone.
            </p>
          </li>
          <li>
            <ion-icon name="keypad-outline" />
            <p>
              Grava todas as teclas digitadas em qualquer aplicativo, utilizando nosso teclado virtual (Whatsapp, Facebook, etc)
            </p>
          </li>
          <li>
            <ion-icon name="radio-outline" />
            <p>
              Escuta Ambiente mesmo com o telefone bloqueado, você pode ouvir o que se passa ao redor , o Celular Vip captura o audio ambiente.
            </p>
          </li>
          <li>
            <ion-icon name="call-outline" />
            <p>
              Ouvir todas as ligações telefônicas, o aplicativo grava a conversa e envia para nossa central de relatórios.
            </p>
          </li>
          <li>
            <ion-icon name="logo-whatsapp" />
            <p>
              O aplicativo monitora todas as conversas de texto realizadas no Whatsapp.
            </p>
          </li>
        </ul>
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
    title: 'Celular VIP :: Universal Detetives'
  }
}
</script>
<style lang="scss" scoped>
  .celular-vip-text{
    ul{
      display: grid;
      list-style: none;
      padding: 0;
      row-gap: 30px;
      column-gap: 30px;
      margin-top: 50px;
      grid-template-columns: 1fr 1fr 1fr;

      @media (max-width: 767.95px) {
        grid-template-columns: 1fr;
      }

      @media (min-width: 767.95px) and (max-width: 991.95px) {
        grid-template-columns: 1fr 1fr;
      }

      li{
        display: flex;
        align-items: flex-start;
        column-gap: 20px;

        ion-icon{
          color: var(--azul);
          font-size: 40px;
          min-width: 40px;
        }
      }
    }
  }
</style>
