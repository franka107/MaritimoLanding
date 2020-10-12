<template>
  <div class="slogan uk-margin-top uk-margin-bottom">
    <div class="uk-flex-center" uk-grid>
      <div class=" uk-flex-center" uk-grid>
        <div class="uk-width-1-3">
          <img width="100" height="100" alt="" :src="svgSrc">
        </div>
        <div class="uk-width-2-3 uk-flex uk-flex-middle uk-flex-center uk-padding-remove">
          <div class=" uk-text-center uk-text-bold uk-text-primarydark">
            {{title}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slogan',
  props: {
    svgSrc: {
      type: String,
      default: require('@/assets/redicon.svg')
    },
    title: {
      type: String,
      default: 'TITULO DE EJEMPLO'
    },
  }
}
</script>

<style scoped>
.slogan {
  width: 270px
}
.uk-text-primarydark {
  color: darkblue;
}
</style>
