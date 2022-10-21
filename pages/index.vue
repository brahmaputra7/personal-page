<template>
  <div>
    <div class="section-1">
      <v-container class="d-flex" style="flex-flow:column; height:100%">
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
                <div><v-btn color="purple darken-4">contact</v-btn></div>
              </div>
          </div>
          <div class="d-flex justify-center align-center" style="flex-grow:1; flex-flow:column  ">
            <div class="mainSection d-flex justify-center pa-10 align-center mb-10" >
              <div style="max-width:750px">
                <v-row class="align-center">
                  <v-col cols="12" md="3" class="d-flex justify-center">
                    <img src="/img/PHOTO.png" width="150px" height="150px">
                  </v-col>
                  <v-col cols="12" md="9" class="pa-10">
                    I’m <b>Brahma Putra</b> —  a UX Engineer based in Bandung. Currently working at Cityplan Indonesia. I started as a front-end developer, I work on most project using and Figma. I merge technical skills with design knowledge to create innovative products that drive business.
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
            <div style="max-width:600px;text-align: center;">
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
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>John Leider</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
        </v-list>
      </v-navigation-drawer>
      
    </div>
    <div class="section-2 wow slideInLeft" >
      <v-container>
        <div class="pa-5 d-flex align-center justify-center" style="flex-flow:column">
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

        <div class="d-flex justify-center my-10" style="flex-flow:row wrap">
          <div>
          <h2>
            Design and <br v-if="!$vuetify.breakpoint.mobile"/>Development<br v-if="!$vuetify.breakpoint.mobile"/>Challange
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
  &:hover {
    transform:scale(1.1);
  }
  transition:1s;
  max-width:800px;
  height:fit-content;
  font-size:1.1em;
  border-radius: 20px;
  background:linear-gradient(277.92deg, #936BB3 -10.28%, #1E0035 -10.28%, #25002C -10.27%, #302B34 88.58%) !important;
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
  background: linear-gradient(90.02deg, #D9D9D9 -10.32%, #A329AD -10.31%, #1F1643 114.18%)
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
      model:null
    }
  },
  methods:{
  }
}
</script>
