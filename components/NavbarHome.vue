<template>
  <header>
    <nav class="nav navbar">
      <div class="container">
        <div class="nav_links">
          <nuxt-link to="" class="nav-link">
            Home
          </nuxt-link>
          <nuxt-link to="" class="nav-link">
            Sobre nós
          </nuxt-link>
          <nuxt-link to="" class="nav-link">
            Serviços
          </nuxt-link>
          <nuxt-link to="" class="nav-link">
            Localidades
          </nuxt-link>
          <nuxt-link to="" class="nav-link">
            Fale conosco
          </nuxt-link>
        </div>
        <div class="nav_redes_sociais">
          <a href="">
            <ion-icon name="logo-twitter" />
          </a>
          <a href="">
            <ion-icon name="logo-facebook" />
          </a>
          <a href="">
            <ion-icon name="logo-instagram" />
          </a>
          <a href="">
            <ion-icon name="logo-pinterest" />
          </a>
          <a href="">
            <ion-icon name="logo-youtube" />
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
  nav{
    margin-bottom: 10px;
    .container{
      display: flex;
      align-items: center;
      justify-content: space-between;

      .nav_links{
        display: flex;

        .nav-link{
          color: white;
          letter-spacing: 1.5px;
          position: relative;
          padding-left: 0 !important;
          padding-right: 0 !important;
          margin-right: 40px;
          text-transform: uppercase;
          font-weight: 300;
          font-size: 14px;
          font-family: 'Audiowide', cursive;

          &:last-child{
            margin-right: 0 !important;
          }

          &::after{
            content: '';
            position: absolute;
            left: 0;
            bottom: 2px;
            width: 0%;
            height: 2px;
            background-color: var(--azul);
            transition: all .3s;
          }

          &:hover{
            &::after{
              width: 100%;
            }
          }
        }
      }

      .nav_redes_sociais{
        display: flex;

        a{
          margin-right: 20px;
          position: relative;

          &:last-child{
            margin-right: 0 !important;
          }

          &::after{
            content: '';
            position: absolute;
            left: 0;
            bottom: -7px;
            width: 0%;
            height: 2px;
            background-color: var(--azul);
            transition: all .3s;
          }

          &:hover{
            &::after{
              width: 100%;
            }
          }

          ion-icon{
            font-size: 25px;
            min-width: 25px;
            width: 100%;
            margin-bottom: -7px !important;
            color: white;
          }
        }
      }
    }
  }
</style>
