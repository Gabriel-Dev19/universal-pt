<template>
  <div>
    <p>{{ name }}</p>
  </div>
</template>
<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['name']
}
</script>
<style lang="scss" scoped>
  div{
    width: auto;
    padding: 4px 13px;
    border-radius: 20px;
    background-color: #c3e4f5;
    margin-bottom: 10px;

    p{
      margin-bottom: 0 !important;
      text-transform: uppercase;
      font-size: 13.3px;
      font-weight: 500 !important;
      color: #00354e;

      @media (max-width: 576px) {
        font-size: 11px;
      }
    }
  }
</style>
