<template>
  <div 
    :class="`uk-background-fixed uk-background-norepeat uk-background-cover uk-background-center-center uk-height-${size} uk-width-1-1 uk-background-blend-multiply uk-background-${backgroundColor}`" 
    :style="`background-image: url(${imageSrc});`">
    <div class="uk-padding">
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Panel',
  props: {
    imageSrc: {
      type: String,
      default: 'https://images.pexels.com/photos/2416606/pexels-photo-2416606.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260'
    },
    backgroundColor: {
      type: String,
      default: 'primary',
      validator: function(value) {
        return [
          'primary',
          'danger',
          'warning',
          'default', 
          'muted',
          'blue',
          'secondary',
          'primarydark'
        ].indexOf(value) !== -1
      }
    },
    size: {
      type: String,
      default: 'large',
      validator: function(value) {
        return [
          'small',
          'medium',
          'large',
        ].indexOf(value) !== -1
      }
    },
  }
}
</script>

<style>
.uk-background-danger {
  background-color: red;
}

.uk-background-warning {
  background-color: yellow;
}

.uk-background-primarydark {
  background-color: darkblue;
}

.uk-background-blue {
  background-color: blue;
}
</style>
