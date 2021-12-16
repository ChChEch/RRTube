<template>
  <nav>
    <v-app-bar class="white" flat app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="font-weight-bold">
    <img src="https://c.tenor.com/x8v1oNUOmg4AAAAC/rickroll-roll.gif" alt="juutub" width="50px"> 
        </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-text-field flat hide-details append-icon="mdi-magnify" placeholder="Search" outlined dense class="hidden-sm-and-down"></v-text-field>
      <v-spacer></v-spacer>
      <v-menu offsetY>
      </v-menu>

      <v-tooltip bottom>
      </v-tooltip>
      <v-tooltip bottom>
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon size="28">mdi-dots-vertical</v-icon></v-btn>        
            <div id="app">
              <p>{{currentDateTime()}}</p>
            </div>
        </template>
      </v-tooltip>            
      <v-btn ripple outlined elevation="2" color="rgb(0, 124, 188)"  >
        <v-icon size="20">mdi-account</v-icon>
        </v-btn>
    </v-app-bar>



<videos></videos>
     <v-navigation-drawer v-model="drawer" app :clipped="$route.name !== 'Watch'" :temporary="$route.name === 'Watch'" id="nav">
      <div tag="div" class="v-navigation-drawer__content" v-bar>
        <v-list dense nav class="py-0" tag="div">
          <v-list-item :class="{'hidden-lg-and-up': $route.name === 'Watch' ? false : true}">
            <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="font-weight-bold">Rickrolltube</v-toolbar-title>
          </v-list-item>
          <v-divider class="hidden-lg-and-up"></v-divider>
          <div v-for="parentItem in items" :key="parentItem.header">
            <v-subheader v-if="parentItem.header" class="pl-3 py-4 subtitle-4 font-weight-bold text-uppercase" >{{ parentItem.header }}</v-subheader
            >
            <v-list-item v-for="(item) in parentItem.pages" :key="item.title" link class="mb-0" router :to="item.link" exactactive-class="active-item">
              <v-list-item-icon v-if="parentItem.header !== 'Subscriptions'">
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title class=" font-weight-mediutle-2">{{item.title}}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
            <v-divider class="mt-2 mb-2"></v-divider>
          </div>

          <span v-for="link in links" :key="link.text">
            <v-btn color="blue-grey" text small>{{ link.text }}</v-btn>
              
          </span>
        </v-list>
        <div class="tm-footer"><v-icon size="18">
          mdi-copyright</v-icon>Google</div>
      </div>
    </v-navigation-drawer>
  </nav>
</template>


<script>
import videos from '../layouts/videos.vue'
export default {
  components: { videos },
  data: () => ({

    drawer: false,
    items: [
      {
        header: null,
        pages: [
          
          { title: 'Home', 
          icon: 'mdi-home' 
          },

          { title: 'Explore', 
          icon: 'mdi-compass-outline' 
          },
          {
            title: 'Subscriptions',
            icon: 'mdi-youtube-subscription'
          }
        ]
      },
      {
        header: null,
        pages: [
          {
            title: 'Library',
            icon: 'mdi-play-box-multiple'
          },
          {
            title: 'History',
            icon: 'mdi-history'
          },

        ]
      },
      {
        header: null,
      },
      {
        pages: [
          {
            title: 'Browse channels',
            
            icon: 'mdi-plus-circle'
          },
        ]
      },
      
      {
        pages: [
          {
            title: 'Rickroll upgrade',
            icon: 'mdi-arm-flex'
          },
          {
            icon: 'mdi-access-point',
            title: 'Live'
          }
        ]
      },

      {
        header: null,
        pages: [
          {
            title: 'Setting',
            icon: 'mdi-cog'
          },
          {
            title: 'Help',
            icon: 'mdi-help-circle'
          },
        ]
        
      }
    ],
header: null,
  }),
    
  mounted() {
    this.drawer = this.$vuetify.breakpoint.mdAndDown ? false : true
    this.drawer = this.$route.name === 'Watch' ? false : this.drawer
  },
methods: {
    currentDateTime() {
      const current = new Date();
      const date = current.getFullYear()+'-'+(current.getMonth()+1)+'-'+current.getDate();
      const time = current.getHours() + ":" + current.getMinutes() + ":" + current.getSeconds();
      const dateTime = date +' '+ time;
      
      return dateTime;
    }
  }
}
</script>
<style scoped>
    #wrapper { 
      width: 650px  ;
      background-color: rgb(255, 255, 255);
    }
    html, body {
      color: grey;
      background-color:rgb(250, 28, 65);
    }
    .white {
      color: rgb(32, 34, 32);
    }
    .tm-footer {
      position: absolute;
      bottom: 0px;
          }
    .vaatab1 {
      font-size: 15px;
    }
</style>