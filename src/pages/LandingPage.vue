<template>
  <div>
    <Panel 
      :imageSrc="firstPanel.imageSrc"
      :backgroundColor="firstPanel.color"
      :size="firstPanel.size"
    >
      <div class=" uk-flex-wrap-reverse uk-flex-center" uk-grid>

        <div class="uk-width-1-2@m">
          <VueSlickCarousel v-bind="settings" :arrows="true" :dots="true">
            <div class="uk-margin-top   " ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="uk-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="uk-margin-top   " ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="uk-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="uk-margin-top   " ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="uk-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
          </VueSlickCarousel>
        </div>
        <div class=" uk-flex uk-flex-middle uk-flex-center">
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
        <div class="uk-card uk-card-default uk-grid-collapse uk-child-width-1-2@s uk-margin" uk-grid>
          <div class="uk-card-media-left uk-cover-container uk-flex uk-flex-center uk-flex-middle">
            <img width="100" height="100" alt="" src="@/assets/redicon.svg" uk-svg>
          </div>
          <div>
            <div class="uk-card-body">
              <div class="uk-card-title">Seguridad y confianza</div>
            </div>
          </div>
        </div>
      </div>

      <div class="uk-flex-center" uk-grid>
        <div class="uk-width-1-5 uk-flex-center" uk-grid>
          <div class="uk-width-1-3">
            <img width="100" height="100" alt="" src="@/assets/redicon.svg" uk-svg>
          </div>
          <div class="uk-width-2-3 uk-flex uk-flex-middle uk-flex-center uk-padding-remove">
            <div class="uk-text-large uk-text-center uk-text-bold uk-text-primary">
              TITULO DE EJEMPLO
            </div>
          </div>
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
        size: "auto"
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
        "autoplay": true,
        "slidesToShow": 3,
        "slidesToScroll": 1,
        "swipeToSlide": true,
        "responsive": [
          {
            "breakpoint": 1366,
            "settings": {
              "slidesToShow": 2,
              "slidesToScroll": 2,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 1100,
            "settings": {
              "slidesToShow": 1,
              "slidesToScroll": 1,
              "initialSlide": 1
            }
          },
          {
            "breakpoint": 960,
            "settings": {
              "slidesToShow": 3,
              "slidesToScroll": 3,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 828,
            "settings": {
              "slidesToShow": 2,
              "slidesToScroll": 2,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 580,
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
  font-size: 55px;
  color: white;
  font-weight:bold;
}

.panel-subtext{
  font-size: 35px;
  color: white
}

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
