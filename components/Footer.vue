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
          routerTo: '/'
        },
        {
          name: 'Investigação conjugal',
          routerTo: '/'
        },
        {
          name: 'Investigação política',
          routerTo: '/'
        },
        {
          name: 'Localização de pessoas',
          routerTo: '/'
        },
        {
          name: 'Celular VIP',
          routerTo: '/'
        },
        {
          name: 'Acompanhamento de filhos',
          routerTo: '/'
        }
      ],
      links_rodape_localidades: [
        {
          name: 'Santa Catarina',
          routerTo: '/'
        },
        {
          name: 'Paraná',
          routerTo: '/'
        },
        {
          name: 'Rio Grande do Sul',
          routerTo: '/'
        },
        {
          name: 'São Paulo',
          routerTo: '/'
        },
        {
          name: 'Rio de Janeiro',
          routerTo: '/'
        },
        {
          name: 'Distrito Federal',
          routerTo: '/'
        },
        {
          name: 'Minas Gerais',
          routerTo: '/'
        },
        {
          name: 'Mato Grosso do Sul',
          routerTo: '/'
        },
        {
          name: 'Goiás',
          routerTo: '/'
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
footer{
  margin-top: 130px;
  padding: 50px 0;
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
}
</style>
