<template>
  <div class="mycard">
    <div class="mycard-header">
      <div class="mycard-title">
        {{name}}
      </div>
    </div>
    <div class="my-card-body uk-padding-small uk-padding-remove-bottom">
      <div class="mycard-price">
        <span class="mycard-currency uk-text-large uk-text-emphasis uk-text-bold">
          {{currency}}
        </span>
        <span class="mycard-price uk-text-extralarge uk-text-emphasis uk-text-bold">
          {{price}}
        </span>
      </div>
      <div v-if="date" class="uk-text-center uk-text-bold  uk-text-emphasis  uk-text-medium mycard-date">{{date}}</div>
      <div class="slogan uk-margin-remove">
          <div class="uk-flex uk-flex-center" uk-grid>
            <div class="uk-width-1-3  uk-flex uk-flex-center uk-flex-middle">
              <img width="40" height="40" alt="" src="https://icons555.com/images/icons-red/image_icon_whatsapp_pic_512x512.png">
            </div>
            <div class="uk-width-2-3 uk-flex uk-flex-middle uk-flex-center uk-padding-remove">
              <div class=" uk-text-center uk-text-bold uk-text-primarydark ">
                <button class=" uk-align-center  mycard-buttoncontact uk-margin-remove">Comienza un plan</button>
              </div>
            </div>
          </div>
      </div>
      <ul class="uk-list uk-list-disc uk-text-small uk-list-primary">
        <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
      </ul>
      <div class="uk-flex uk-flex-center">
        <button class=" uk-align-center    mycard-button ">¡Comprar Paquete!</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'MyDetailedCard',
  props: {
    name: {
      type:String,
      default: 'PAQUETE 0'
    },
    price: {
      type:String,
      default: '0,00'
    },
    date: {
      type: String,
    },
    currency: {
      type: String,
      default: 'us'
    },
    benefits: {
      type:Array,
      default: () => ( [
        'here are many variations of passages of Lorem ',
        'here are many variations of passages of Lorem ',
        'here are many variations of passages of Lorem ',
        'here are many variations of passages of Lorem ',
        'here are many variations of passages of Lorem ',
      ]),
    }
  }
}
</script>
<style scoped>
.mycard {
   border-color: #FA0200;
   max-width: 340px;
   min-height: 150px;
   border: 2px solid red;
   border-radius: 18px;
   //box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.mycard-header {
   height: 45px;
   background: #FA0200;
   color: white;
   font-weight: 400;
   border-radius: 13px 13px 0 0;
   display: flex;
   align-items: center;
   justify-content: center;
   font-size: 18px;
}
.mycard-price { 
   display: flex;
   justify-content: center;
   align-items: center;
}
.mycard-button {
    background-color: #FA0200;
    color: white;
    border: 1px solid #FA0200;
    border-radius: 13px;
    text-transform: none;
    display: inline-block;
    padding: 0 50px;
    vertical-align: middle;
    font-size: 16px;
    font-weight: bold;
    line-height: 30px;
    text-align: center;
    text-decoration: none;
}

.mycard-button:hover{
    background: darkblue;
    border: 1px solid darkblue;
    color: #fff;
    cursor: pointer;
}
.mycard-button:focus{
    outline: none;
}

.mycard-buttoncontact {
    background-color: white;
    color: #FA0200;
    border: 1px solid #FA0200;
    border-radius: 13px;
    text-transform: none;
    display: inline-block;
    padding: 0 50px;
    vertical-align: middle;
    font-size: 12px;
    font-weight: bold;
    line-height: 30px;
    text-align: center;
    text-decoration: none;
    min-width: 220px
}

.mycard-buttoncontact:hover{
    background: #FA0200;
    color: #fff;
    cursor: pointer;
}
.mycard-buttoncontact:focus{
    outline: none;
}
.uk-text-extralarge {
  font-size: 2.3rem
}
.uk-text-medium {
  font-size: 1.3rem
}
</style>
