<template>
  <div>
    <Panel 
      :imageSrc="firstPanel.imageSrc"
      :backgroundColor="firstPanel.color"
      :size="firstPanel.size"
      style="padding-left: 100px; padding-rigth:100px"
    >
      <div class="uk-flex uk-flex-center">
        <div class="uk-width-1-2@m">
          <VueSlickCarousel v-bind="settings" :arrows="true" :dots="true">
            <div class=""><MyCardV2/></div>
            <div class=""><MyCardV2/></div>
            <div class=""><MyCardV2/></div>
            <div class=""><MyCardV2/></div>
          </VueSlickCarousel>
        </div>
        <div class="uk-width-1-2@m uk-flex uk-flex-middle uk-flex-center">
          <div >
            <div class="uk-text-center panel-text-large ">¡DESTACATÉ!</div>
            <div class="panel-subtext uk-text-center">y pauta con nosotros</div>
            <button class=" uk-align-center    mybutton ">QUIERO DESTACARME</button>
          </div>
        </div>
      </div>
    </Panel>
    <div class="uk-padding">
      <div class="uk-flex uk-flex-center">
        <div>
          <div class="uk-card uk-card-default uk-card-body">Item</div>
        </div>
      </div>
    </div>
    <div class="uk-padding">
      <div class="uk-padding uk-text-lead uk-text-center uk-text-bold">ANUNCIOS DESTACADOS</div>
      <div class="uk-flex uk-flex-center">
        <div class="uk-width-1-2@m">
          <div class="uk-text-center">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</div>
        </div>
      </div>
    </div>
    <Panel 
      :backgroundColor="secondPanel.color"
      :size="secondPanel.size"
    />
    <div class="uk-padding uk-flex-center   "  uk-grid>
      <div><MyCard price="7,99" date="2 Semanas" name="PAQUETE 1"/></div>
      <div><MyCard date="1 Semana"/></div>
      <div><MyCard/></div>
    </div>
  </div>
</template>

<script>
import Panel from '@/components/Panel'
import MyCard from '@/components/MyCard'
import MyCardV2 from '@/components/MyCardV2'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  name: 'LandingPage',
  props: {
    
  },
  components: {
    Panel,
    MyCard,
    MyCardV2,
    VueSlickCarousel
  },
  data() {
    return {
      firstPanel:{
        imageSrc: "https://images.pexels.com/photos/2935097/pexels-photo-2935097.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260%202520w",
        color: "danger",
        size: "large"
      },
      secondPanel:{
        color: "blue",
        size: "medium"
      },
      settings: {
        "dots": true,
        "infinite": true,
        "initialSlide": 2,
        "speed": 500,
        "slidesToShow": 3,
        "slidesToScroll": 1,
        "swipeToSlide": true,
        "responsive": [
          {
            "breakpoint": 1024,
            "settings": {
              "slidesToShow": 3,
              "slidesToScroll": 3,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 600,
            "settings": {
              "slidesToShow": 2,
              "slidesToScroll": 2,
              "initialSlide": 2
            }
          },
          {
            "breakpoint": 480,
            "settings": {
              "slidesToShow": 1,
              "slidesToScroll": 1
            }
          }
        ]
      }
    }
  }
}
</script>

<style>

.panel-text-large{
  font-size: 50px;
  color: white;
  font-weight:bold;
}

.panel-subtext{
  font-size: 30px;
  color: white
}

.mybutton {
    background-color: white;
    color: #FA0200;
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

.mybutton:hover{
    background: darkblue;
    border: 1px solid darkblue;
    color: #fff;
    cursor: pointer;
}
.mybutton:focus{
    outline: none;
}
</style>
