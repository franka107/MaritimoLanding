<template>
  <div class="mycard">
    <div class="mycard-header">
      <div class="mycard-title uk-text-bold">
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
          <div class="uk-flex uk-flex-center uk-flex-middle" uk-grid>
            <div class="  uk-flex uk-flex-center uk-flex-middle">
              <span class="uk-align-center uk-flex uk-flex-center uk-flex-middle whatsapp-red"   uk-icon="icon: whatsapp; ratio: 1.8"></span>
            </div>
            <div class="uk-flex uk-flex-middle uk-flex-center uk-padding-remove">
              <div class=" uk-text-center uk-text-bold uk-text-primarydark ">
                <button class=" uk-align-center  mycard-buttoncontact ">¡Contactar un asesor!</button>
              </div>
            </div>
          </div>
      </div>
      <ul class="uk-list uk-list-disc uk-text-small uk-list-primary">
        <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
      </ul>
    </div>
    <div class="my-card-footer uk-margin-bottom ">
      <div class="uk-flex uk-flex-center uk-flex-bottom">
        <button class="mycard-button ">¡Comprar Paquete!</button>
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
      default: 'PLAN 0'
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
   width: 340px;
   border: 1px solid red;
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

.my-card-body {
  min-height: 400px
  
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
    border-radius: 18px;
    text-transform: none;
    display: inline-block;
    margin: 0 15px;
    padding: 0 25px;
    vertical-align: middle;
    font-size: 17px;
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

.my-card-footer {
}
</style>
