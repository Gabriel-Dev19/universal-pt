<template>
  <header>
    <nav class="navbar py-0 nav">
      <div class="container">
        <a href="" class="logo_navbar_redes_sociais">
          <img src="../assets/img/logo-universal.webp" width="130" alt="Logo Universal Detetives particulares">
        </a>
        <div class="mae_redes_sociais">
          <a href="">
            <ion-icon name="logo-twitter" />
            <i class="fas fa-sort-up" />
          </a>
          <a href="">
            <ion-icon name="logo-facebook" />
            <i class="fas fa-sort-up" />
          </a>
          <a href="">
            <ion-icon name="logo-instagram" />
            <i class="fas fa-sort-up" />
          </a>
          <a href="">
            <ion-icon name="logo-pinterest" />
            <i class="fas fa-sort-up" />
          </a>
          <a href="">
            <ion-icon name="logo-youtube" />
            <i class="fas fa-sort-up" />
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
  a:hover{
    text-decoration: none !important;
  }

  nav{
    box-shadow: 0 0.1rem 0.3rem rgba(0, 0, 0, 0.234) !important;
    height: 73px;
    align-items: center;
  }

  .container{
    display: flex;
    flex-wrap: wrap;
    justify-content: end;
    position: relative;
    padding-top: 20px;
    padding-bottom: 20px;
    align-items: center;
    height: 100%;

    .logo_navbar_redes_sociais{
      position: absolute;
      top: 10px;
      left: 0;
    }

    .mae_redes_sociais{
      display: flex;

      a{
        margin-right: 17px;
        color: var(--azul);
        display: flex;
        flex-wrap: wrap;
        justify-content: center;

        ion-icon{
          font-size: 27px;
          min-width: 27px;
          width: 100%;
          margin-bottom: -7px !important;
        }

        i{
          opacity: 0;
          transform: translateY(15px);
          transition: all .3s;
          margin-bottom: -9px !important;
        }

        &:hover i{
          opacity: 1;
          transform: translateY(9px);
        }

        &:last-child{
          margin-right: 0 !important;
        }
      }
    }
  }
</style>
