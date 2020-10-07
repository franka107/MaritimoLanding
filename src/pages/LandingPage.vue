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
    <div class="uk-padding uk-padding-remove-bottom uk-flex-center" uk-grid>
      <Slogan title="OTRO TITULO DE EJEMPLO"/>
      <Slogan/>
      <Slogan/>
      <Slogan/>
      <Slogan/>

    </div>
    <div class="uk-padding">
      <div class="uk-padding uk-padding-remove-top uk-text-lead uk-text-center uk-text-bold">ANUNCIOS DESTACADOS</div>
      <div class="uk-flex uk-flex-center">
        <div class="uk-width-1-2@m">
          <div class="uk-text-center">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</div>
        </div>
      </div>
    </div>
    <Panel 
      :backgroundColor="secondPanel.color"
      :size="secondPanel.size"
    >
      <div class=" uk-text-large  uk-text-center uk-text-bold uk-text-light">¡Realiza tu primer destacado en solo 3 pasos!</div>
      <div class="uk-padding uk-padding-remove-bottom uk-flex-center" uk-grid>
        <NumberSlogan/>
        <NumberSlogan number="1"/>
        <NumberSlogan/>
      </div>
    </Panel>
    <div class="uk-padding uk-padding-remove-bottom uk-flex-center   "  uk-grid>
      <div><MyCard price="7,99" date="2 Semanas" name="PAQUETE 1"/></div>
      <div><MyCard date="1 Semana"/></div>
      <div><MyCard/></div>
    </div>
    <button class=" uk-align-center mybutton mybutton--red ">Iniciar sesión</button>
    <div class="uk-padding uk-padding-remove-top uk-padding-remove-bottom uk-text-lead uk-text-center uk-text-bold">¿NO TIENES UNA CUENTA?</div>
    <div class="uk-padding uk-padding-remove-top uk-text-lead uk-text-center uk-text-bold">CREALA POR PRIMERA VEZ Y CONOCE TODOS NUESTROS BENEFICIOS</div>
    <div class="uk-padding uk-padding-remove-bottom uk-flex-center   "  uk-grid>
      <div class="uk-width-1-3@m">
        <ul class="uk-list uk-list-disc uk-list-primary">
          <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
        </ul>
      </div>
      <div class="uk-width-1-3@m">
        <ul class="uk-list uk-list-disc uk-list-primary">
          <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
        </ul>
      </div>
    </div>
    <button class=" uk-align-center mybutton mybutton--red ">Crear Cuenta</button>
    <Panel 
      :backgroundColor="thirdPanel.color"
      :size="thirdPanel.size"
      imageSrc=""
    >
      <div class="uk-padding uk-padding-remove-bottom uk-padding-remove-top uk-flex-center   "  uk-grid>
        <div><span class="uk-icon-button" uk-icon="icon: chevron-right; ratio: 2"></span></div>
        <div class=" uk-text-large uk-flex uk-flex-middle  uk-text-center uk-text-bold uk-text-light uk-margin-right uk-margin-left">¿Cómo crear mi cuenta y destacar mi anuncio?</div>
        <div>
          <button class="uk-margin-remove  uk-align-center mybutton mybutton--red ">Saber más</button>
        </div>
      </div>
    </Panel>
    <Panel 
      :backgroundColor="fourthPanel.color"
      :size="fourthPanel.size"
      :imageSrc="fourthPanel.imageSrc"
      class="panel-shortmargin"
    ></Panel>
    <div class="uk-padding">
      <div class="uk-padding uk-padding-remove-top uk-text-lead uk-text-center uk-text-bold">OTROS PLANES - CONTENIDOS</div>
      <div class="uk-padding uk-padding-remove-top uk-padding-remove-bottom  uk-text-center ">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt </div>
      <div class="uk-padding uk-padding-remove-top uk-padding-remove-bottom  uk-text-center ">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt 
        <span class="uk-text-bold">text of the printing and typesetting industry. </span>
      </div>
    </div>
    <div class="uk-padding  uk-flex-center   "  uk-grid>
      <div><MyDetailedCard price="7,99" date="2 Semanas" name="PAQUETE 1"/></div>
      <div><MyDetailedCard date="1 Semana"/></div>
      <div><MyDetailedCard/></div>
      <div><MyDetailedCard/></div>
    </div>
    <Panel 
      :backgroundColor="fifthPanel.color"
      :size="fifthPanel.size"
      :imageSrc="fifthPanel.imageSrc"
    >
      <div >
        <div class="uk-flex uk-flex-middle">
          <span class="uk-align-center whatsapp-white"   uk-icon="icon: whatsapp; ratio: 3.5"></span>
        </div>
        <div class="uk-text-light uk-text-center">Consigue muchos mas benefecios con nuestro contacto ademas de promociones y novedades</div>
      </div>
      <button class=" uk-align-center mybutton--transparent ">Crear Cuenta</button>
    </Panel>
  </div>
</template>

<script>
import Panel from '@/components/Panel'
import MyCard from '@/components/MyCard'
import MyDetailedCard from '@/components/MyDetailedCard'
import MyCardV2 from '@/components/MyCardV2'
import Slogan from '@/components/Slogan'
import NumberSlogan from '@/components/NumberSlogan'
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
    MyDetailedCard,
    MyCardV2,
    VueSlickCarousel,
    Slogan,
    NumberSlogan,
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
        size: "auto"
      },
      thirdPanel:{
        color: "primarydark",
        size: "auto"
      },
      fourthPanel:{
        imageSrc: "https://images.pexels.com/photos/2935097/pexels-photo-2935097.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260%202520w",
        color: "danger",
        size: "large"
      },
      fifthPanel:{
        imageSrc: "https://images.pexels.com/photos/2935097/pexels-photo-2935097.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260%202520w",
        color: "primarydark",
        size: "auto"
      },
      benefits: [
        'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsu',
        'here are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form,',
        'here are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form,',
        'here are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form,',
        'here are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form,',
        'here are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form,',
      ],

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

.mybutton--red {
    background-color: #FA0200;
    color: white ;
}

.mybutton--transparent {
    color: white;
    background: transparent;
    border: 1px solid white;
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
.mybutton--transparent:hover{
    background: red;
    border: 1px solid red;
    color: #fff;
    cursor: pointer;
}
.mybutton--transparent:focus{
    outline: none;
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

.uk-text-light{
  color: white;
}

.panel-shortmargin{
  margin-top: 10px
}
.whatsapp-white svg path {
  fill: white;
}
</style>
