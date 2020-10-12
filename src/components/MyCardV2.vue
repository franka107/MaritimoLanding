<template>
    <div>
      <div class="uk-card uk-card-default mycardV2 ">
          <div class="uk-card-media-top ">
              <img class="mycardV2-image" :src="imageSrc" alt="">
          </div>
          <div class="uk-card-body uk-padding-small">
              <div class="mycardV2-title  uk-text-bold uk-text-emphasis">{{title}}</div>
              <div class="mycardV2-subtitle uk-text-small uk-text-danger uk-text-bold">{{subtitle}}</div>
              <div class="uk-text-small">{{description}}</div>
              <button class=" uk-margin-small-top  uk-align-center   mycardV2-button ">{{button}}</button>
          </div>
      </div>
    </div>
</template>
<script>
export default {
  name: 'MyCardV2',
  props: {
    imageSrc: {
      type: String,
      default: 'https://images.pexels.com/photos/533937/pexels-photo-533937.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260'
    },
    title: {
      type: String,
      default: 'El titulo'
    },
    subtitle: {
      type: String,
      default: 'El subtitulo'
    },
    description: {
      type: String,
      default: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.'
    },
    button: {
      type: String,
      default: 'Me interesa'
    },
  }
}
</script>
<style>
.mycardV2 {
  min-width: 220px;
  max-width: 255px;
  border-radius: 8px;
  -webkit-box-shadow: 3px 4px 7px 1px rgba(0,0,0,0.4);
  -moz-box-shadow: 3px 4px 7px 1px rgba(0,0,0,0.4);
  box-shadow: 3px 4px 7px 1px rgba(0,0,0,0.4);
}


.mycardV2-image{
  border-radius: 8px 8px 0 0;
}

.mycardV2-button {
    background-color: #FA0200;
    color: white;
    border: 1px solid #FA0200;
    border-radius: 18px;
    text-transform: none;
    display: inline-block;
    padding: 0 40px;
    vertical-align: middle;
    font-size: 14px;
    font-weight: bold;
    line-height: 30px;
    text-align: center;
    text-decoration: none;
}

.mycardV2-button:hover{
    background: #FA0200;
    color: #fff;
    cursor: pointer;
}
.mycardV2-button:focus{
    outline: none;
}
</style>
