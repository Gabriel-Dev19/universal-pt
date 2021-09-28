<template>
  <section>
    <div class="row position-relative mx-auto align-items-start col-12 px-0" :class="{'justify-content-end': !isReverse}">
      <div class="img_header_section col-sm-6 col-lg-4 col-xl-5 position-absolute px-0" :class="{'right-0': isReverse, 'left-0': !isReverse}">
        <img :src="img" class="shadow border" alt="">
      </div>
      <div class="col-11 col-sm-8 col-lg-9 col-xl-8 content_header_section">
        <div class="row mx-0 col-lg-5 px-0">
          <Badge :name="titleBadge" />
          <h2 class="col-12 px-0">
            <span class="text-azul-escuro"> {{ parteAzul }} </span> {{ titleHeader }}
          </h2>
        </div>
        <div class="col-lg px-0 ml-lg-5 mt-4 mt-lg-0">
          <h5>
            {{ subtitle }}
          </h5>
          <p>
            {{ description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import Badge from './Badge.vue'
export default {
  components: { Badge },
  props: {
    isReverse: {
      type: Boolean,
      default: false
    },
    img: {
      type: String,
      default: ''
    },
    parteAzul: {
      type: String,
      default: ''
    },
    titleHeader: {
      type: String,
      default: ''
    },
    subtitle: {
      type: String,
      default: ''
    },
    description: {
      type: String,
      default: ''
    },
    titleBadge: {
      type: String,
      default: ''
    }
  }
}
</script>
<style lang="scss" scoped>
  section{
    .img_header_section{
      height: 400px;

      img{
        height: 100%;
        width: 100%;
        object-fit: cover;
        border-radius: 0 45px 0 45px;
      }

      &.right-0{
        right: 0;
      }

      &.left-0{
        left: 0;
      }
    }

    .content_header_section{
      margin-top: 50px;
      background-color: white;
      box-shadow: 0 0.1rem 1rem rgba(0, 0, 0, 0.255) !important;
      padding: 35px;
      border-radius: 25px;
      display: flex;
      flex-wrap: wrap;
      align-items: start;

      @media (max-width: 576px) {
        margin-top: 200px;
        padding: 20px;
      }

      h5{
        font-weight: 700;
        letter-spacing: 0.3px;
      }

      p{
        font-size: 15px;
        margin-bottom: 0 !important;
      }
    }
  }
</style>
