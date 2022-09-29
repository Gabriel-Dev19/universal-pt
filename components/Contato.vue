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
          Preencha nosso formulário de contato abaixo e um especialista entrará em contato com você.
          Ou fale pelos canais de atendimento {{ VarificaAoLado }}
        </p>
      </div>
      <div class="row col-12 mt-3 px-0 mx-0">
        <form class="row col-xl-7 px-0 justify-content-between mx-0" @submit.prevent="submit">
          <div v-if="showMsgFixSuccess" class="py-1 bg-success rounded d-flex align-items-center col-12 text-white mb-3 px-2">
            <ion-icon class="mr-2" style="min-width: 19px; font-size: 19px" name="checkmark-circle-outline" />
            Mensagem enviada com sucesso
          </div>
          <div class="form-group">
            <input v-model="nome" type="text" class="form-control" placeholder="Seu nome">
            <div v-show="ShowMsgError" v-if="$v.nome.$error" class="error">
              Este campo é obrigatório, mínimo {{ $v.nome.$params.minLength.min }} letras.
            </div>
          </div>
          <div class="form-group">
            <input
              v-model="telefone"
              v-mask="mask"
              type="text"
              class="form-control"
              placeholder="Seu telefone"
            >
            <div v-show="ShowMsgError" v-if="$v.telefone.$error" class="error">
              Preencha com um telefone válido
            </div>
          </div>
          <div class="form-group">
            <input v-model="email" type="text" class="form-control" placeholder="Seu e-mail">
            <div v-show="ShowMsgError" v-if="$v.email.$error" class="error">
              Digite um e-mail válido
            </div>
          </div>
          <div class="form-group">
            <input v-model="cidade" type="text" class="form-control" placeholder="Cidade">
            <div v-show="ShowMsgError" v-if="$v.cidade.$error" class="error">
              Digite sua cidade
            </div>
          </div>
          <div class="form-group">
            <input v-model="estado" type="text" class="form-control" placeholder="Estado">
            <div v-show="ShowMsgError" v-if="$v.estado.$error" class="error">
              Digite seu estado
            </div>
          </div>
          <div class="form-group">
            <select v-model="tipo_servico" class="col-12 form-control px-0">
              <option value="" disabled selected>
                Selecione o serviço...
              </option>
              <option value="Investigação empresarial">
                Investigação empresarial
              </option>
              <option value="Investigação conjugal">
                Investigação conjugal
              </option>
              <option value="Investigação política">
                Investigação política
              </option>
              <option value="Localização de pessoas">
                Localização de pessoas
              </option>
              <option value="Curso de detetive particular">
                Curso de detetive particular
              </option>
              <option value="Celular VIP">
                Celular VIP
              </option>
              <option value="Acompanhamento de filhos">
                Acompanhamento de filhos
              </option>
            </select>
            <div v-show="ShowMsgError" v-if="$v.tipo_servico.$error" class="error">
              Informe o tipo de serviço
            </div>
          </div>
          <div class="form-group">
            <select v-model="tipo_pessoa" class="col-12 form-control px-0">
              <option value="" disabled selected>
                Tipo de pessoa...
              </option>
              <option value="Pessoa física">
                Pessoa física
              </option>
              <option value="Pessoa jurídica">
                Pessoa jurídica
              </option>
            </select>
            <div v-show="ShowMsgError" v-if="$v.tipo_pessoa.$error" class="error">
              Informe o tipo de pessoa
            </div>
          </div>
          <div class="form-group">
            <input v-model="data_e_horario" type="text" class="form-control" placeholder="Data e hora para contato">
            <div v-show="ShowMsgError" v-if="$v.data_e_horario.$error" class="error">
              Informe uma data e horário
            </div>
          </div>
          <div class="form-group col-12 px-0">
            <textarea v-model="mensagem" class="form-control" placeholder="Sua mensagem aqui" />
            <div v-show="ShowMsgError" v-if="$v.mensagem.$error" class="error">
              Digite uma mensagem
            </div>
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
    <b-modal
      id="modal-success"
      ref="ModalSuccess"
      centered
      size="md"
      hide-footer
      hide-header
      @hide="EventHideModal"
    >
      <div class="py-4 mt-1 modal-body-success px-3">
        <div class="d-flex justify-content-center">
          <ion-icon name="checkmark-circle-outline" />
        </div>
        <h5 class="text-white mt-2 text-center">
          Mensagem enviada com sucesso!
        </h5>
        <p class="text-white text-center">
          Sua mensagem será enviada para nossa central de atendimento e logo entraremos
          em contato.
        </p>
        <div class="d-flex mb-2 justify-content-center">
          <button class="btn btn-outline-light" @click="$refs.ModalSuccess.hide()">
            OK
          </button>
        </div>
      </div>
    </b-modal>
  </section>
</template>
<script>
import Vue from 'vue'
import Vuelidate from '../node_modules/vuelidate'
import axios from '../node_modules/axios'
import { required, email, minLength } from '../node_modules/vuelidate/lib/validators'
import { VueMaskDirective } from '../node_modules/v-mask'
import Badge from './parts/Badge.vue'
Vue.use(Vuelidate)
Vue.directive('mask', VueMaskDirective)
export default {
  components: { Badge },
  data () {
    return {
      nome: '',
      email: '',
      telefone: '',
      cidade: '',
      estado: '',
      tipo_servico: '',
      data_e_horario: '',
      tipo_pessoa: '',
      mensagem: '',

      showMsgFixSuccess: false,

      ShowMsgError: true,

      newNumberTelefone: '',
      oldNumeberTelefone: '',

      mask: '(##) ####-####',

      redes_sociais: [
        { icon: 'twitter', href: '' },
        { icon: 'facebook', href: '' },
        { icon: 'instagram', href: '' },
        { icon: 'pinterest', href: '' },
        { icon: 'youtube', href: '' }
      ],
      telefones: [
        {
          cidade: 'Florianópolis',
          numero: '+55 (48) 4052-8425',
          href: 'tel:4840528425'
        },
        {
          cidade: 'Baln. Camboriú',
          numero: '+55 (47) 4054-9580',
          href: 'tel:4740549580'
        },
        {
          cidade: 'Curitiba',
          numero: '+55 (41) 4063-9171',
          href: 'tel:4140639171'
        },
        {
          cidade: 'Caçador',
          numero: '+55 (49) 3240-0977',
          href: 'tel:4932400977'
        }
      ]
    }
  },
  computed: {
    VarificaAoLado () {
      return window.innerWidth > 1200 ? 'ao lado' : 'a baixo'
    }
  },
  validations: {
    nome: {
      required,
      minLength: minLength(3)
    },
    email: {
      required,
      email
    },
    telefone: {
      required,
      minLength: minLength(14)
    },
    cidade: {
      required
    },
    estado: {
      required
    },
    tipo_servico: {
      required
    },
    data_e_horario: {
      required
    },
    tipo_pessoa: {
      required
    },
    mensagem: {
      required
    }
  },
  watch: {
    telefone (newNumber, oldNumeber) {
      if (newNumber.length === 15) {
        this.mask = '(##) #####-####'
      }
      if (newNumber.length < 15) {
        this.mask = '(##) ####-####'
      }
    }
  },
  methods: {
    submit () {
      this.$v.$touch()
      if (this.$v.$invalid === false) {
        axios.defaults.headers.post['Content-Type'] = 'application/x-www-form-urlencoded'
        axios.post('http://universaldetetives.com.br/envio.php', JSON.stringify({
          nome: this.nome,
          email: this.email,
          telefone: this.telefone,
          cidade: this.cidade,
          estado: this.estado,
          tipo_servico: this.tipo_servico,
          data_e_horario: this.data_e_horario,
          mensagem: this.mensagem,
          tipo_pessoa: this.tipo_pessoa
        }))
          .then(
            setTimeout(() => {
              this.$refs.ModalSuccess.show()
              this.ShowMsgError = false
              this.nome = ''
              this.email = ''
              this.telefone = ''
              this.cidade = ''
              this.estado = ''
              this.tipo_servico = ''
              this.data_e_horario = ''
              this.mensagem = ''
              this.tipo_pessoa = ''
            }, 300)
          )
      }
    },
    EventHideModal () {
      this.showMsgFixSuccess = true
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
          width: 48%;
          margin-bottom: 13px !important;

          .error{
            color: var(--danger);
            font-size: 14px;
            letter-spacing: 0.1px;
          }

          input{
            margin-bottom: 5px;
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
            margin-bottom: 5px;
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

          textarea{
            margin-bottom: 5px;
            padding-top: 10px !important;
            padding-bottom: 21px !important;
            background-color: var(--cinza_claro);
            // box-shadow: 0 0rem 0.2rem rgba(0, 0, 0, 0.111) !important;
            border: none !important;
            border-radius: 0 !important;
            font-size: 17px;
            min-height: 120px;
            max-height: 120px;

            &::placeholder{
              font-weight: 500 !important;
              font-size: 17px;
            }

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
