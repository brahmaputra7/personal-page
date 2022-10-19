<template>
  <div class="section-1">
    <v-container>
        
        <div class="d-flex justify-space-between py-10">
            <div><img src="/img/BRAHMALAB.png" width="150px"></div>
            <div v-if="$vuetify.breakpoint.mobile">
              <v-btn
                color="pink"
                dark
                @click.stop="drawer = !drawer"
              >
                <v-icon>mdi-menu</v-icon>
              </v-btn>
              <v-navigation-drawer
                  v-model="drawer"
                  absolute
                  right
                  temporary
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
                    <v-list-item
                      v-for="item in items"
                      :key="item.title"
                      link
                    >
                      <v-list-item-icon>
                        <v-icon>{{ item.icon }}</v-icon>
                      </v-list-item-icon>

                      <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                      </v-list-item-content>
                    </v-list-item>
                  </v-list>
                </v-navigation-drawer>
            </div>
            <div v-else class="d-flex align-center">
              <div class="mr-5">HOME</div>
              <div class="mr-5">CURRICULUM VITAE</div>
              <div><v-btn color="purple darken-4">contact</v-btn></div>
            </div>
        </div>
        <div class="mainSection d-flex justify-center pa-10 align-center mb-10" >
          <div style="max-width:750px">
            <v-row class="align-center">
              <v-col cols="12" md="3" class="d-flex justify-center">
                <img src="/img/PHOTO.png" width="150px" height="150px">
              </v-col>
              <v-col cols="12" md="9" class="pa-10">
                I’m <b>Brahma Putra</b> —  a UX Engineer based in Bandung. Currently working at Cityplan Indonesia. I started as a front-end developer, I work on most project using NuxtJS. I merge technical skills with design knowledge to create innovative products that drive business.
              </v-col>
            </v-row>
          </div>
        </div>
    </v-container>
  </div>
</template>

<style>
.section-1 {
  background:url('/img/bg.jpg');
}
.mainSection {
  min-height:350px;
  font-size:1.1em;
  background: linear-gradient(277.92deg, #FF0099 -10.28%, #880052 -10.27%, #4E008B 88.58%);
  border-radius: 30px;
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
  data(){
    return {
      drawer:false
    }
  }
}
</script>
