<template>
  <button 
    @mouseover="hover = true"
    @mouseleave="hover = false"
    class="uk-margin-remove uk-align-center mybutton"
    :class="{ active: hover }"
  >{{title}}</button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    title: {
      type: String,
      default: 'El botón'
    },
    color: {
      type: String,
      default: 'red'
    },
    backgroundColor: {
      type: String,
      default: 'white'
    }
  },
  data() {
    return{
      hover: false,
    }
  }
}
</script>

<style>
.mybutton {
    background-color: white;
    color: #FA0200;
    border: 1px solid #FA0200;
    border-radius: 19px;
    text-transform: none;
    display: inline-block;
    padding: 0 50px;
    vertical-align: middle;
    font-size: 16px;
    font-weight: bold;
    line-height: 40px;
    text-align: center;
    text-decoration: none;
}

.active{
    background: darkblue;
    border: 1px solid darkblue;
    color: #fff;
    cursor: pointer;
}
.mybutton:focus{
    outline: none;
}

</style>
