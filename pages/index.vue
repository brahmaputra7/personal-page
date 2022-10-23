<template>
  <div>
    <div class="navbarPersonal" :class="{'change_color': scrollPosition > 50}">
      <v-container>
      <div class="d-flex justify-space-between align-center" >
              <div><img src="/img/BRAHMALAB.png" width="150px"></div>
              <div v-if="$vuetify.breakpoint.mobile">
                <v-btn
                  color="pink"
                  dark
                  @click.stop="drawer = !drawer"
                >
                  <v-icon>mdi-menu</v-icon>
                </v-btn>
              </div>
              <div v-else class="navMenus d-flex align-center">
                <a class="mr-5" href="#section-2"><b>Highlight</b></a>
                <a class="mr-5" href="#section-2"><b>Background</b></a>
                <div class="mr-5" @click="contact=true"><b>Project</b></div>
                <div class="mr-5" @click="contact=true"><b>Publication</b></div>
                <div class="mr-5"><b><a href="/pdf/Brahma-CV.pdf" download="" target="blank">Curicculum Vitae</a></b></div>
                <div><v-btn color="purple darken-4" @click="contact=true">contact</v-btn></div>
              </div>
          </div>
        </v-container>
    </div>
    <div class="section-1" >
      <v-container class="d-flex" style="flex-flow:column; min-height:800px">
          <div class="d-flex justify-center align-center" style="flex-grow:1; flex-flow:column  ">
            <div class="mainSection d-flex justify-center pa-10 align-center mb-10" data-aos-delay="100">
              <div style="max-width:750px">
                <v-row class="align-center">
                  <v-col cols="12" md="3" class="d-flex justify-center">
                    <img src="/img/PHOTO.png" width="150px">
                  </v-col>
                  <v-col cols="12" md="9" class="pa-2">
                    I’m <b>Brahma Putra</b> —  a UX Engineer of <a class="white--text" href="https://cityplan.id" target="_blank">Cityplan Indonesia</a>. I started as a front-end developer, I work on most project using NuxtJS and Figma. I merge technical skills with design knowledge to create innovative products that drive business. Mostly build tools for spatial analysis and public services.
                  </v-col>
                </v-row>
              </div>
            </div>
            <div>
              <div>
                <center>
                 Skill Tags:
                </center>
            </div>
            <div class="mb-10" style="max-width:600px;text-align: center;">
              <v-chip class="mr-b mt-2">User Experience (UX)</v-chip>
              <v-chip class="mr-b mt-2">Front-end Development</v-chip>
              <v-chip class="mr-b mt-2">GIS Development</v-chip>
              <v-chip class="mr-b mt-2">Usability Testing</v-chip>
              <v-chip class="mr-b mt-2">Figma</v-chip>
              <v-chip class="mr-b mt-2">VueJS</v-chip>
              <v-chip class="mr-b mt-2 purple">View More</v-chip>

            </div>
            </div>
        </div>
      </v-container>

      
      <v-navigation-drawer
        v-model="drawer"
        v-if="drawer"
        right
        absolute
      >
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>
              <b>HOME</b>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>
              <b><a href="/pdf/Brahma-CV.pdf" class="white--text" download="" target="blank" style="text-decoration:none">DOWNLOAD MY CV</a></b>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title>
              <v-btn color="purple darken-4" @click="contact=true">contact</v-btn>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
        </v-list>
      </v-navigation-drawer>
      
    </div>
    <div id="section-2" class="section-2 wow slideInLeft" >
      <v-container>
        <div class="pa-5 d-flex align-center justify-center mt-10" style="flex-flow:column" data-aos="fade-up">
          <h2>Product Highlight - Dash Spatia</h2>
          <div class="purpleLine my-5" 
      data-aos="flip-right"></div>
          <div style="max-width: 800px">
            <center>Dash is a spatial tools and analytical app that helps user analyzing spatial data with multiple tools. Dash is bringing multiple spatial datasets and a growing library of spatial analysis tools to help people do their location research faster and more efficient anywhere.</center>
          </diV>
        </div>
      </v-container>

      <v-sheet
      data-aos="fade-up"
          class="mx-auto"
          elevation="8"
        >
          <v-slide-group
            v-model="model"
            class="pa-4"
            active-class="success"
            show-arrows
          >
            <v-slide-item
              v-for="n in 6"
              :key="n"
              v-slot="{ active }"
            >
              <v-card
                :color="active ? undefined : 'grey lighten-1'"
                class="ma-4"
                width="300"
              >
              <img :src="'/img/'+n+'.jpg'" width="100%"/>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>

        <div class="d-flex justify-center my-10 pa-3" style="flex-flow:row wrap" 
          data-aos="fade-up">
          <div>
          <h2>
            Design and <br v-if="!$vuetify.breakpoint.mobile"/>Development <br v-if="!$vuetify.breakpoint.mobile"/>Challange
          </h2>
        </div>
          <div class="ml-3 pl-3" style="max-width:800px;text-align:left; border-left:7px solid white;">
            Dash growing tools and modules will help automate and accelerate your location research work. Dash is capable to tailor your need to turn the data into a location insight using a custom-made module for your company and client specific workflow. The most challangin part dash is feature scalability.
          </div>
        </div>

        <div class="videoSection" 
      data-aos="zoom-in-up">
          <video autoplay loop muted="muted" controlslist="nodownload" src="/img/spatia.mp4"></video>
        </div>
        
        <div class="d-flex justify-center my-5">
          <v-btn class="white red--text mt-3" rounded style="width:250px" href="https://spatia.id" target="_blank">LEARN MORE</v-btn>
        </div>
      

    </div>

    <div class="menupadSection pt-10 mt-10 pb-10">
        <div class="section-2 wow slideInLeft">
          <v-container>
            <div class="pa-5 d-flex align-center justify-center" style="flex-flow:column" data-aos="fade-up">
              <h2>Project Highlight - Menupad</h2>
              <div class="whiteLine my-5"  data-aos="flip-right"></div>
              <div style="max-width: 800px"  data-aos="fade-up">
                <center>Menupad helps culinary businesses to provide digital menus, automate whatsapp orders and organize online store links or social media for your business. Unlike print menus which are hard to see on small screens. Direct your customers to digital menus specially designed for smartphone screens.

                This menu can be accessed via a QR code, or via a link on your social media profile.</center>
              </diV>
            </div>
          </v-container>
        </div>
  
      <v-sheet
       data-aos="fade-up"
          class="mx-auto elevation-0"
          elevation="8"
          style="background-color: transparent;"
        >
          <v-slide-group
            v-model="model"
            class="pa-4"
            active-class="success"
            show-arrows
          >
            <v-slide-item
              v-for="n in 8"
              :key="n"
            >
              <v-card
                class="ma-4 elevation-0"
                  width="200"
                  style="background-color:transparent"
              >
              <img :src="'/img/m'+n+'.png'" width="100%"/>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </v-sheet>
        
        <div class="d-flex justify-center align-center"  data-aos="fade-up">
            <div class="mb-5" style="text-align:center;max-width:800px">
              Receive orders or pre-orders with a special format via whatsapp?

    Help your customers make ordering easier.

    Customers can select the menu and send details of the shipping address. No more need to write order writing format.
    Want to direct customers to your online store, social media channels or food delivery service?

The menupad provides a page for storing those links, one where it's all there.
            </div>
      </div>

        <v-container data-aos="fade-up pb-10">
          <v-row>
            <v-col md="3" cols="12" class="videoSection">
              <video autoplay loop muted="muted" controlslist="nodownload" src="/img/menupad.mp4"></video>
            </v-col>
            <v-col md="9" cols="12">
              <img class="elevation-4" width="100%" src="/img/menupad-header.png" style="border-radius:10px">
              <h2>Design and Development Challange</h2>
              Dash growing tools and modules will help automate and accelerate your location research work. Dash is capable to tailor your need to turn the data into a location insight using a custom-made module for your company and client specific workflow. The most challangin part dash is feature scalability. <br/>
              <v-btn class="white red--text mt-3" rounded style="width:250px" href="https://spatia.id" target="_blank">LEARN MORE</v-btn>
            </v-col>
          </v-row>
      </v-container>

    </div>

    <div class="projectListSection pa-10">
      
      <div class="d-flex align-center justify-center" style="flex-flow:column" data-aos="fade-up">
        <h1>Projects</h1>
        <div class="purpleLine mb-8 mt-3"></div>
      </div>

      <div style="text-align:center;overflow-x:auto"  data-aos="fade-up">
        <v-btn-toggle
            v-model="projectListToggle"
            rounded
          >
            <v-btn>
              All
            </v-btn>
            <v-btn>
              Location Intelligence
            </v-btn>
            <v-btn>
              Public Services
            </v-btn>
            <v-btn>
              Machine Learning
            </v-btn>
            <v-btn>
              Others
            </v-btn>
          </v-btn-toggle>
      </div>
    </div>

    <div>
      <v-container>
        <v-row>
          <v-col cols="12" md="4" v-for="item,index in projectData" :key="index" style="height:350px">
            <div class="projectContainer">
              <div class="pa-5 d-flex align-space-between" style="flex-flow:row wrap">
                <img :src="'/img/' + item.thumbnail " width="100%"/>
                <div>
                  <h3>{{item.title}}</h3>
                  <div style="font-size:0.8em">{{item.descriptiton}}</div>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
    </v-container>
    </div>

    <v-dialog v-model="contact" width="500px">
      <v-card class="pa-5">
        <v-icon class="mr-2">mdi-email</v-icon> brahmaputra1996@gmail.com<br/>
        <v-divider class="my-2"></v-divider>
        <v-icon class="mr-2" >mdi-whatsapp</v-icon> 085862266465
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  created(){
  },
  data(){
    return {
      drawer:false,
      model:null,
      contact:false,
      scrollPosition:null,
      projectListToggle:'',
      projectData:[
        {
          title:'Patrol Taru Pusat',
          descriptiton:'Spatial monitoring and control center. Integrating data from all across indonesia.',
          thumbnail:'patrolpusat.png',
          category:''
        },
        {
          title:'RDTR Interaktif',
          descriptiton:'Interaktif Spatial Plan of Indonesia. Featured in Online Single Submision (OSS) website.',
          thumbnail:'rdtrinteraktif.png',
        },
        {
          title:'Composite Credit Rating',
          descriptiton:'Rating and Assessment comparison from multiple source like S&P, Moodys, and Fitch.',
          thumbnail:'ccr.png',
        },
        {
          title:'Teletherapy Mobile App',
          descriptiton:'a Mobile app for online doctor consultation.',
          thumbnail:'teletherapy.png',
        },
        {
          title:'Covid 19 Information Center',
          descriptiton:'Covid 19 global information visualization from various notable sources.',
          thumbnail:'covidinfo.png',
        },
        {
          title:'Covid 19 Prediction System',
          descriptiton:'Prediction covid19 infection status based on medical condition.',
          thumbnail:'covid-prediction.png',
        }
      ]
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  },
  methods:{
    updateScroll() {
       this.scrollPosition = window.scrollY
    }
  },
}
</script>

<style lang="scss">
.projectContainer {
  background-color:#262626;
  border-radius:20px;
  height:300px;
  width:100%;
}

.navMenus {
  div {
    &:hover {
      transition:0.4s;
      a {
        transition:0.4s;
        
      color:purple !important;
      }
      color:purple !important;
    }
  }
  cursor:pointer;
  a {
    color:#fff !important; text-decoration: none;
  }
}

.navbarPersonal {
  position:fixed;
  display:flex;
  align-items: center;
  top:0;
  width:100%;
  height:80px;
  z-index:999;
}

.section-1 {
  background:url('/img/bg.jpg');
  width:100%;
  min-height:100vh;
}
.mainSection {
  transition:1s;
  max-width:800px;
  height:fit-content;
  font-size:1.1em;
  border-radius: 20px;
  background: linear-gradient(96.63deg, #260631 44.79%, #270058 90.71%) !important;
  box-shadow:20px -1px 134px 47px #000000 !important;
}


.videoSection {
  display:flex;
  justify-content: center;
  video {
    border-radius:10px;
    width:100%;
    max-width:1000px;
  }
}

.purpleLine {
  height:10px;
  width:300px;
  border-radius:20px;
  background: linear-gradient(90.02deg, #D9D9D9 -10.32%, #A329AD -10.31%, #1F1643 114.18%);
}

.whiteLine {
  height:10px;
  width:300px;
  border-radius:20px;
  
  background: linear-gradient(90deg, rgba(217, 217, 217, 0.83) 1.82%, rgba(217, 217, 217, 0.27) 100.01%);
}

.change_color {
  transition:1s;
  height:60px;
  background-color:#000;
  padding:0;
}

.menupadSection {
  background: linear-gradient(96.63deg, #850038 44.79%, #8E3300 90.71%);
}
</style>
