<template>
        <v-app>
                 <v-navigation-drawer  app   clipped  fixed  v-model="sideNav"  >
                        <v-list>
                                <v-list-tile
                                         v-for="item in menuItems" 
                                         :key="item.title"
                                          :to="item.link">
                                        <v-list-tile-action>
                                                <v-icon>{{ item.icon }}</v-icon>
                                        </v-list-tile-action>
                                        <v-list-tile-content>
                                                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                                        </v-list-tile-content>
                                </v-list-tile>
                        </v-list>
                </v-navigation-drawer>

                <v-toolbar dark  app  fixed clipped-left  class="error">
                        <v-toolbar-side-icon @click="sideNav = !sideNav" class="hidden-sm-and-up "></v-toolbar-side-icon>
                        <v-toolbar-title>
                                <router-link to="/" tag="span" style="cursor : pointer">DevMeetup</router-link>
                        </v-toolbar-title>
                        <v-spacer></v-spacer>
                        <v-toolbar-items class="hidden-xs-only">
                                <v-btn flat 
                                        v-for="item in menuItems" 
                                        v-bind:key="item.title"
                                         :to="item.link">
                                        <v-icon left>{{ item.icon }}</v-icon>
                                        {{ item.title }}
                                </v-btn>
                        </v-toolbar-items>
                </v-toolbar>

                <main>
                        <router-view></router-view>
                </main>
                        
                
               
        </v-app>
</template>

<script>
export default {
  data() {
    return {
            sideNav : false,
            menuItems: [
                    { icon : ' supervisor_account ', title : '  View Meetups ', link: {name: 'Meetups'}},
                    { icon : ' room ', title : ' Organize Meetup ', link: {name: 'CreateMeetup'} },
                    { icon : ' person ', title : ' Profile ',link: {name: 'Profile'} },
                    { icon : ' face ', title : ' Sign up ' , link: {name: 'Signup'}},
                    { icon : ' lock_open ', title : ' Sign in ' , link: {name: 'Signin'}}
            ]
      
    }
  },
  name: 'App'
}
</script>
