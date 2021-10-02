<template>
  <footer>
    <div class="container">
      <div class="col-12 d-flex justify-content-center justify-content-xl-start mb-4 px-0">
        <div>
          <img src="../assets/img/logo-universal-sem-nome.webp" width="150" alt="">
        </div>
      </div>
      <div class="col-xl mr-xl-5 px-0">
        <p class="text-center text-xl-left">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae ullam fugiat adipisci soluta
        </p>
        <p class="text-center text-xl-left">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae
        </p>
        <div class="row justify-content-center justify-content-xl-start mt-4 mx-0">
          <a v-for="item in redes_sociais" :key="item.icon" :href="item.href" class="links_quadrados_redes_sociais">
            <div class="caixa-icon">
              <ion-icon :name="`logo-${item.icon}`" />
            </div>
          </a>
        </div>
      </div>
      <div class="col-xl-6 px-0 row mt-5 pt-5 pt-xl-0 mt-xl-0 mx-0">
        <div class="col-sm px-0">
          <h5 style="font-weight: 600">
            Serviços:
          </h5>
          <div v-for="item in links_rodape_servicos" :key="item.name" class="d-flex">
            <nuxt-link :to="item.routerTo" class="link-seta cinza mt-2">
              {{ item.name }}
              <div class="mae_seta">
                <div class="seta">
                  <ion-icon name="chevron-forward-outline" />
                </div>
              </div>
            </nuxt-link>
          </div>
        </div>
        <div class="col-sm px-0 mt-5 mt-sm-0 ml-sm-5">
          <h5 style="font-weight: 600">
            Localidades atendidas:
          </h5>
          <div v-for="item in links_rodape_localidades" :key="item.name" class="d-flex">
            <nuxt-link :to="item.routerTo" class="link-seta cinza mt-2">
              {{ item.name }}
              <div class="mae_seta">
                <div class="seta">
                  <ion-icon name="chevron-forward-outline" />
                </div>
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <div class="notas">
      <div class="container">
        <p class="mb-0 text-center text-lg-left col-lg px-0">
          &copy; Copyright - Universal Detetives - Todos os direitos reservados
        </p>
        <a class="text-center text-lg-right col-lg px-0" href="https://wa.me/5588996912604?text=Olá,+Gabriel+gostaria+de+receber+mais+informações+sobre+seu+trabalho+como+programador" target="_blank" rel="noopener noreferrer">
          Projetado e desenvolvido por Gabriel Camurça <ion-icon name="logo-vue" />
        </a>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  data () {
    return {
      redes_sociais: [
        { icon: 'twitter', href: '' },
        { icon: 'facebook', href: '' },
        { icon: 'instagram', href: '' },
        { icon: 'pinterest', href: '' },
        { icon: 'youtube', href: '' }
      ],
      links_rodape_servicos: [
        {
          name: 'Investigação empresarial',
          routerTo: '/servicos/investigacao-empresarial'
        },
        {
          name: 'Investigação conjugal',
          routerTo: '/servicos/investigacao-conjugal'
        },
        {
          name: 'Investigação política',
          routerTo: '/servicos/investigacao-politica'
        },
        {
          name: 'Localização de pessoas',
          routerTo: '/servicos/localizacao-de-pessoas'
        },
        {
          name: 'Celular VIP',
          routerTo: '/servicos/celular-VIP'
        },
        {
          name: 'Acompanhamento de filhos',
          routerTo: '/servicos/acompanhamento-de-filhos'
        },
        {
          name: 'Curso de detetive',
          routerTo: '/servicos/curso-de-detetive-particular'
        }
      ],
      links_rodape_localidades: [
        { name: 'Santa Catarina', routerTo: '/detetive-particular-em-Santa-Catarina' },
        { name: 'Paraná', routerTo: '/detetive-particular-no-Parana' },
        { name: 'Rio Grande do Sul', routerTo: '/detetive-particular-no-Rio-Grande-do-Sul' },
        { name: 'São Paulo', routerTo: '/detetive-particular-em-Sao-Paulo' },
        { name: 'Rio de Janeiro', routerTo: '/detetive-particular-no-Rio-de-Janeiro' },
        { name: 'Distrito Federal', routerTo: '/detetive-particular-no-Distrito-Federal' },
        { name: 'Minas Gerais', routerTo: '/detetive-particular-em-Minas-Gerais' },
        { name: 'Mato Grosso do Sul', routerTo: '/detetive-particular-no-Mato-Grosso-do-Sul' },
        { name: 'Goiás', routerTo: '/detetive-particular-em-Goias' }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
footer{
  margin-top: 130px;
  padding-top: 50px;
  box-shadow: 0 -0.1rem 0.5rem rgba(0, 0, 0, 0.35) !important;

  .container{
    display: flex;
    flex-wrap: wrap;

    .caixa-icon{
      background-color: var(--cinza_claro);
      width: 35px;
      height: 35px;
      display: flex;
      justify-content: center;
      align-items: center;

      ion-icon{
        font-size: 23px;
        min-width: 23px;
        color: #6c757d;
      }
    }

    .links_quadrados_redes_sociais{
      margin-right: 15px;

      &:last-child{
        margin-right: 0 !important;
      }
    }
  }

  .notas{
    margin-top: 50px;
    padding: 20px 0;
    background-color: var(--cinza_claro);

    .container{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      font-weight: 500;

      a{
        color: var(--grafite) !important;

        ion-icon{
          font-size: 20px;
          min-width: 20px;
          margin-bottom: -4px;
        }
      }
    }

  }
}
</style>
