<template>
  <section id="contato">
    <div class="container">
      <div class="row mae_tema mx-0">
        <div class="col-12 d-flex px-0">
          <Badge name="contato" />
        </div>
        <h2 class="col-lg-9 px-0">
          Entre em contato com nossa equipe!
        </h2>
        <p class="col-lg-9 mt-2 px-0">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Temporibus porro
          veniam dolorum possimus ratione beatae eligendi quaerat dolore
        </p>
      </div>
      <div class="row col-12 px-0 mx-0">
        <form action="" method="post" class="row col-xl-7 px-0 justify-content-between mx-0">
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Seu nome">
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Seu telefone">
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Digite um e-mail válido">
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Diga sua cidade">
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Diga seu estado">
          </div>
          <div class="form-group">
            <select name="" class="col-12 form-control px-0">
              <option value="" disabled selected>
                Selecione o serviço...
              </option>
              <option value="">
                Investigação empresarial
              </option>
              <option value="">
                Investigação conjugal
              </option>
            </select>
          </div>
          <div class="form-group">
            <select name="" class="col-12 form-control px-0">
              <option value="" disabled selected>
                Tipo de pessoa...
              </option>
              <option value="">
                Pessoa física
              </option>
              <option value="">
                Pessoa jurídica
              </option>
            </select>
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Hora para contato">
          </div>
          <div class="form-group">
            <input type="text" class="form-control" placeholder="Data para contato">
          </div>
          <div class="d-flex mt-3 justify-content-end col-12 px-0">
            <button type="submit" class="btn btn-azul-lg">
              Enviar formulário
            </button>
          </div>
        </form>
        <div class="ml-xl-5 px-0 mt-5 mt-xl-3 col-xl">
          <div class="contatos_description px-0">
            <ion-icon name="at-outline" />
            <div class="col px-0 ml-2 mt-2">
              <h6>
                Redes sociais:
              </h6>
              <div class="row mt-3 mx-0">
                <a v-for="item in redes_sociais" :key="item.icon" :href="item.href" class="mr-2">
                  <div class="caixa-icon">
                    <ion-icon :name="`logo-${item.icon}`" />
                  </div>
                </a>
              </div>
            </div>
          </div>
          <div class="contatos_description mt-4 pt-2 px-0">
            <ion-icon name="call-outline" />
            <div class="col px-0 ml-2 mt-2">
              <h6 class="mb-3">
                Telefones:
              </h6>
              <a v-for="item in telefones" :key="item.cidade" :href="item.href" class="d-block mt-2">
                <span class="col-12 d-block px-0 text-grafite">
                  <b>{{ item.cidade }}</b> {{ item.numero }}
                </span>
              </a>
            </div>
          </div>
          <div class="contatos_description overflow-hidden mt-4 pt-2 px-0">
            <ion-icon name="mail-outline" />
            <div class="col pl-0 pr-4 ml-2 mt-2">
              <h6 class="mb-3">
                E-mail:
              </h6>
              <a href="" class="d-block px-0">
                <span class="text-grafite d-block col-11 px-0" style="word-wrap: break-word;">contato@universaldetetives.com.br</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import Badge from './parts/Badge.vue'
export default {
  components: { Badge },
  data () {
    return {
      redes_sociais: [
        { icon: 'twitter', href: '' },
        { icon: 'facebook', href: '' },
        { icon: 'instagram', href: '' },
        { icon: 'pinterest', href: '' },
        { icon: 'youtube', href: '' }
      ],
      telefones: [
        {
          cidade: 'Baln. Camboriú',
          numero: '+55 (47) 8543-3553',
          href: ''
        },
        {
          cidade: 'Florianópolis',
          numero: '+55 (47) 8543-3553',
          href: ''
        },
        {
          cidade: 'Lages',
          numero: '+55 (47) 8543-3553',
          href: ''
        },
        {
          cidade: 'Curitiba',
          numero: '+55 (47) 8543-3553',
          href: ''
        }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
  section{
    margin-top: 150px;

    .mae_tema{
      max-width: 700px;
    }

    .container{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;

      form{
        width: 100% !important;

        .form-group{
          width: 47%;

          &:nth-child(9){
            width: 100%;
          }

          input{
            margin-top: 17px;
            padding-top: 21px !important;
            padding-bottom: 21px !important;
            background-color: var(--cinza_claro);
            // box-shadow: 0 0rem 0.2rem rgba(0, 0, 0, 0.111) !important;
            border: none !important;
            border-radius: 0 !important;
            font-size: 17px;

            &::placeholder{
              font-weight: 500 !important;
              font-size: 17px;
            }

            &:focus{
              box-shadow: none !important;
            }
          }

          select{
            margin-top: 17px;
            height: 42px;
            background-color: var(--cinza_claro);
            // box-shadow: 0 0rem 0.2rem rgba(0, 0, 0, 0.111) !important;
            border: none !important;
            border-radius: 0 !important;
            font-weight: 500;
            text-indent: 8px;
            font-size: 17px;
            color: #6c757d;
            cursor: pointer;

            &:focus{
              box-shadow: none !important;
            }
          }
        }
      }

      .contatos_description{
        display: flex;

        h6{
          font-weight: 600;
        }

        ion-icon{
          font-size: 32px;
          min-width: 32px;
          color: var(--azul);
        }

        span.text-grafite{
          font-weight: 500;
        }

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
  }
</style>
