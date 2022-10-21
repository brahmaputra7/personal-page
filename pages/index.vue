<template>
  <div>
    <div class="section-1">
      <v-container class="d-flex" style="flex-flow:column; min-height:800px">
          <div class="d-flex justify-space-between align-center py-10">
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
                <div class="mr-5"><b>HOME</b></div>
                <div class="mr-5"><b><a href="/pdf/Brahma-CV.pdf" download="" target="blank">CURRICULUM VITAE</a></b></div>
                <div><v-btn color="purple darken-4" @click="contact=true">contact</v-btn></div>
              </div>
          </div>
          <div class="d-flex justify-center align-center" style="flex-grow:1; flex-flow:column  ">
            <div class="mainSection d-flex justify-center pa-10 align-center mb-10" >
              <div style="max-width:750px">
                <v-row class="align-center">
                  <v-col cols="12" md="3" class="d-flex justify-center">
                    <img src="/img/PHOTO.png" width="150px" height="150px">
                  </v-col>
                  <v-col cols="12" md="9" class="pa-2">
                    I’m <b>Brahma Putra</b> —  a UX Engineer based in Bandung. Currently working at Cityplan Indonesia. I started as a front-end developer, I work on most project using NuxtJS and Figma. I merge technical skills with design knowledge to create innovative products that drive business.
                  </v-col>
                </v-row>
              </div>
            </div>
            <div>
              <div>
                <center>
                 Skill Tags
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
    <div class="section-2 wow slideInLeft" >
      <v-container>
        <div class="pa-5 d-flex align-center justify-center mt-10" style="flex-flow:column">
          <h2>Project Highlight - Dash Spatia</h2>
          <div class="purpleLine my-5"></div>
          <div style="max-width: 800px">
            <center>Dash is a spatial tools and analytical app that helps user analyzing spatial data with multiple tools. Dash is bringing multiple spatial datasets and a growing library of spatial analysis tools to help people do their location research faster and more efficient anywhere.</center>
          </diV>
        </div>
      </v-container>

      <v-sheet
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
              v-slot="{ active, toggle }"
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

        <div class="d-flex justify-center my-10 pa-3" style="flex-flow:row wrap">
          <div>
          <h2>
            Design and <br v-if="!$vuetify.breakpoint.mobile"/>Development <br v-if="!$vuetify.breakpoint.mobile"/>Challange
          </h2>
        </div>
          <div class="ml-3 pl-3" style="max-width:800px;text-align:left; border-left:7px solid white;">
            Dash growing tools and modules will help automate and accelerate your location research work. Dash is capable to tailor your need to turn the data into a location insight using a custom-made module for your company and client specific workflow. The most challangin part dash is feature scalability.
          </div>
        </div>

        <div class="videoSection">
          <video autoplay loop muted="muted" controlslist="nodownload" src="/img/spatia.mp4"></video>
        </div>
        
        <div class="d-flex justify-center my-5">
          <v-btn style="width:350px" class="purple darken-4" rounded>Read More</v-btn>
        </div>
      

    </div>

    <div class="menupadSection pt-10 mt-10">
        <div class="section-2 wow slideInLeft">
          <v-container>
            <div class="pa-5 d-flex align-center justify-center" style="flex-flow:column">
              <h2>Project Highlight - Menupad</h2>
              <div class="whiteLine my-5"></div>
              <div style="max-width: 800px">
                <center>Menupad helps culinary businesses to provide digital menus, automate whatsapp orders and organize online store links or social media for your business. Unlike print menus which are hard to see on small screens. Direct your customers to digital menus specially designed for smartphone screens.

                This menu can be accessed via a QR code, or via a link on your social media profile.</center>
              </diV>
            </div>
          </v-container>
        </div>
  
      <v-sheet
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
              v-slot="{ active, toggle }"
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
        
        <div class="d-flex justify-center align-center">
            <div class="mb-5" style="text-align:center;max-width:800px">
              Receive orders or pre-orders with a special format via whatsapp?

    Help your customers make ordering easier.

    Customers can select the menu and send details of the shipping address. No more need to write order writing format.
    Want to direct customers to your online store, social media channels or food delivery service?

The menupad provides a page for storing those links, one where it's all there.
            </div>
      </div>

        <v-container>
          <v-row>
            <v-col md="3" cols="12" class="videoSection">
              <video autoplay loop muted="muted" controlslist="nodownload" src="/img/menupad.mp4"></video>
            </v-col>
            <v-col md="9" cols="12">
              <img class="elevation-4" width="100%" src="/img/menupad-header.png" style="border-radius:10px">
              <h2>Design and Development Challange</h2>
              Dash growing tools and modules will help automate and accelerate your location research work. Dash is capable to tailor your need to turn the data into a location insight using a custom-made module for your company and client specific workflow. The most challangin part dash is feature scalability. <br/>
              <v-btn class="white red--text mt-3" rounded style="width:250px">READ MORE</v-btn>
            </v-col>
          </v-row>
      </v-container>

    </div>

    <div>
      asdasdasda
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

<style lang="scss">
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

.menupadSection {
  background: linear-gradient(96.63deg, #850038 44.79%, #8E3300 90.71%);
}
</style>

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
      contact:false
    }
  },
  methods:{
  }
}
</script>
