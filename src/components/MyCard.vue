<template>
  <div class="mycard">
    <div class="mycard-header">
      <div class="mycard-title uk-text-bold">
        {{name}}
      </div>
    </div>
    <div class="my-card-body uk-padding uk-padding-remove-bottom  uk-padding-remove-top" >
      <div class="mycard-price">
        <span class="mycard-currency uk-text-large uk-text-emphasis uk-text-bold">
          {{currency}}
        </span>
        <span class="my-card-ammount uk-text-extralarge uk-text-emphasis uk-text-bold">
          {{price}}
        </span>
      </div>
      <div class="uk-text-center uk-text-bold  uk-text-emphasis  uk-text-medium mycard-date">{{date}}</div>
      <button class=" uk-align-center    mycard-button ">¡Comprar Paquete!</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'MyCard',
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
      default: '0 semanas'
    },
    currency: {
      type: String,
      default: 'us'
    },
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

.mycard-title { 
  font-size:20px
}
.mycard-button {
    background-color: white;
    color: #FA0200;
    border: 1px solid #FA0200;
    border-radius: 13px;
    text-transform: none;
    display: inline-block;
    padding: 0 40px;
    vertical-align: middle;
    font-size: 17px;
    font-weight: bold;
    line-height: 30px;
    text-align: center;
    text-decoration: none;
}

.mycard-button:hover{
    background: #FA0200;
    color: #fff;
    cursor: pointer;
}
.mycard-ammount{
  font-size: 40px
}


.mycard-button:focus{
    outline: none;
}
.uk-text-extralarge {
  font-size: 2.7rem;
  padding-top: 20px
}
.uk-text-medium {
  font-size: 1.3rem
}

</style>
