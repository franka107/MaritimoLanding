<template>
  <div>
    <Panel 
      :imageSrc="firstPanel.imageSrc"
      :backgroundColor="firstPanel.color"
      :size="firstPanel.size"
    >
      <div class=" uk-flex-wrap-reverse uk-flex-center" uk-grid>

        <div class="uk-width-1-2@m">
          <VueSlickCarousel :dots="true" class="uk-padding uk-padding-remove-top uk-padding-remove-bottom" v-bind="settings" >
            <template #nextArrow="">
              <span class="arrow-white uk-icon uk-margin-right"  uk-icon="icon: chevron-right; ratio: 2" ></span>
            </template>
            <template #prevArrow="">
              <span class="arrow-white uk-icon "  uk-icon="icon: chevron-left; ratio: 2" ></span>
            </template>
            <div class="mycardV2-margin-top" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="mycardV2-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="mycardV2-margin-top" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="mycardV2-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="mycardV2-margin-top" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
            <div class="mycardV2-margin-bottom" ><MyCardV2 class="uk-flex uk-flex-center"/></div>
          </VueSlickCarousel>
        </div>
        <div class="uk-margin uk-visible@l"></div>
        <div class="uk-margin uk-visible@l"></div>

        <div class=" uk-flex uk-flex-middle uk-flex-center">
          <div >
            <div class="uk-text-center panel-text-large ">¡DESTACATÉ!</div>
            <div class="panel-subtext uk-text-center">y pauta con nosotros</div>
            <button class=" uk-align-center mybutton mybutton-white">QUIERO DESTACARME</button>
          </div>
        </div>
      </div>
    </Panel>
    <div class="uk-padding uk-padding-remove-bottom uk-padding-remove-top uk-flex-center" uk-grid>
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
        <ul class="uk-list uk-list-disc uk-list-danger">
          <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
        </ul>
      </div>
      <div class="uk-width-1-3@m">
        <ul class="uk-list uk-list-disc uk-list-danger">
          <li :key="index" v-for="(benefit, index) in benefits">{{benefit}}</li>
        </ul>
      </div>
    </div>
    <button class=" uk-align-center mybutton mybutton--red ">¡Crear Cuenta!</button>
    <Panel 
      :backgroundColor="thirdPanel.color"
      :size="thirdPanel.size"
      imageSrc=""
    >
      <div class="uk-padding uk-padding-remove-bottom uk-padding-remove-top uk-flex-center   "  uk-grid>
        <div class=" uk-text-large uk-flex uk-flex-middle  uk-text-center uk-text-bold uk-text-light uk-margin-right uk-margin-left">
          <div> 
            <span class="uk-visible@m" uk-icon="icon: chevron-right; ratio: 2"></span>
          </div>
          <div> 
            ¿Cómo crear mi cuenta y destacar mi anuncio?
          </div>
        </div>
        <div>
          <button class="uk-margin-remove  uk-align-center mybutton mybutton--red ">¡Ver Ahora!</button>
        </div>
      </div>
    </Panel>
    <Panel 
      :backgroundColor="fourthPanel.color"
      :size="fourthPanel.size"
      :imageSrc="fourthPanel.imageSrc"
      class="panel-shortmargin"
    >
      <div class="uk-flex uk-flex-center" uk-grid>
        <div>
          <img src="https://lh3.googleusercontent.com/proxy/Iw_S1k-7OAnQ0hpjO0cBdpdF6YSK0ZV1PCkJYsgNsQu_ULCmuLeUYuoew9rJs4-AdB22ZYAvg6Y0STlU_zOIBfp13Z2J7jhDAYssIzmNRiwl_kmRQJK-PRzlbzij-vCDTg" alt="">  
        </div>
        <div class=" uk-flex uk-flex-column uk-flex-wrap-stretch	">
            <div class="panel-subtext uk-text-center">Conoce nuestros planes</div>
            <div class="uk-text-center panel-text-large ">DE CONTENIDO</div>
            <div class="uk-text-center panel-text-large ">DIGITAL</div>
            <button class=" uk-align-center mybutton mybutton-white ">CONOCER PLANES</button>
        </div>
      </div>
    </Panel>
    <div class="uk-padding">
      <div class="uk-padding uk-padding-remove-top uk-text-lead uk-text-center uk-text-bold">OTROS PLANES - CONTENIDOS</div>
      <div class="uk-padding uk-padding-remove-top uk-padding-remove-bottom  uk-text-center ">
        Te ofrecemos todas nuestras plataformas digitales:
      </div>
      <div class="uk-padding uk-padding-remove-top uk-padding-remove-bottom  uk-text-center ">
        Redes sociales, Web, Blog y Mailing para darte a conocer y
        <span class="uk-text-bold"> mejorar tu alcance con tus clientes potenciales. </span>
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
        color: "oceanblue",
        size: "auto"
      },
      fourthPanel:{
        imageSrc: "https://images.pexels.com/photos/2935097/pexels-photo-2935097.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260%202520w",
        color: "danger",
        size: "auto"
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
        "dotsClass": "mydots ",
        "infinite": true,
        "initialSlide": 2,
        "speed": 500,
        "autoplay": true,
        "slidesToShow": 3,
        "slidesToScroll": 3,
        "arrows": true,
        "swipeToSlide": true,
        "responsive": [
          {
            "breakpoint": 1850,
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
    font-size: 20px;
    line-height: 35px;
    border-radius: 25px;
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

.whatsapp-red svg path {
  fill: red;
}

.arrow-white svg  {
  color: white;
  max-width: 5em;
}
.slick-next:before {
  content: ''
}
.slick-prev:before {
  content: '';
}

.mycardV2-margin-top {
  margin-top: 60px
}

.mycardV2-margin-bottom {
  margin-bottom: 60px
}

.mydots {
  display: block;
  width: 100%;
  padding: 0;
  margin: 0;
  margin-top: 25px;
  list-style: none;
  text-align: center;
}

.mydots li {
    position: relative;
    display: inline-block;
    width: 20px;
    height: 20px;
    margin: 0 5px;
    padding: 0;
    cursor: pointer;
}

.mydots li button {
    font-size: 0;
    line-height: 0;
    display: block;
    width: 20px;
    height: 20px;
    padding: 5px;
    cursor: pointer;
    color: transparent;
    border: 0;
    outline: none;
    background: transparent;
}

.mydots li button:before {
    font-family: 'slick';
    border: 2px solid white;
    border-radius: 10px;
    font-size: 11px;
    line-height: 13px;
    position: absolute;
    top: 0;
    left: 0;
    width: 12px;
    height: 12px;
    content: '•';
    text-align: center;
    //opacity: 0.5;
    color: transparent;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

.mydots li.slick-active button:before {
    color: white;
    background-color: white
}

.uk-list-danger > ::before {
  color: red !important;
  font-size: 20px
}

.mybutton-white {
  border: none;
}
</style>





