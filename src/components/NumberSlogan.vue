<template>
  <div class="numberslogan uk-margin-top uk-margin-bottom">
    <div class="uk-flex-center" uk-grid>
      <div class=" uk-flex-center" uk-grid>
        <div class="uk-width-1-3">
          <div class="number uk-flex uk-flex-center">{{number}}</div>
        </div>
        <div class="uk-width-2-3 uk-flex uk-flex-middle uk-flex-center uk-padding-remove">
          <div class="uk-text-small uk-text-center uk-text-light uk-text-primarydark">
            {{description}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NumberSlogan',
  props: {
    description: {
      type: String,
      default: 'Esta es una propiedad -description- incluida por defecto en el componente, aparecera si no esta pasando esta propiedad por medio del componente padre.'
    },
    number: {
      type: String,
      default: '0'
    }
  }
}
</script>
<style scoped>
.uk-text-light{
  color: white;
}
.numberslogan {
  width: 470px
}
.number {
  color: red;
  font-weight: bold;
  font-size: 90px
}
</style>
