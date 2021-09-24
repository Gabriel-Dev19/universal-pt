<template>
  <footer>
    <div class="container">
      <div class="col-12 mb-4 px-0">
        <img src="../assets/img/logo-universal-sem-nome.webp" width="150" alt="">
      </div>
      <div class="col-lg-6 px-0">
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae ullam fugiat adipisci soluta
        </p>
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae adipisicing elit. Sunt quam rem dicta praesentium.
          Libero cumque placeat error repudiandae
        </p>
        <div class="row mt-4 mx-0">
          <a v-for="item in redes_sociais" :key="item.icon" :href="item.href" class="mr-3">
            <div class="caixa-icon">
              <ion-icon :name="`logo-${item.icon}`" />
            </div>
          </a>
        </div>
      </div>
      <div class="col-lg-6 row mx-0">
        <div class="col-6">
          <h5 style="font-weight: 600">
            Serviços
          </h5>
        </div>
        <div class="col-6">
          <h5 style="font-weight: 600">
            Localidades atendidas
          </h5>
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
  }
}
</style>
