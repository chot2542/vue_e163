<template>
    <!-- App.vue -->

<v-app>

    <v-system-bar
          color="#708090"
          :height="height"
          :lights-out="lightsOut"
          :window="window"
        >
          <v-icon>mdi-signal-cellular-outline</v-icon>
          <span>AIS</span>
          &nbsp;<v-icon>mdi-wifi-strength-4</v-icon>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          <span>12:30</span>
          <v-spacer></v-spacer>
          <v-icon>mdi-battery</v-icon>
          <span>100%</span>
        </v-system-bar>
        
  <v-navigation-drawer app>
    <!-- -->
  </v-navigation-drawer>

<div>
       <v-app-bar color="#fccd14"densedark>

      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab><b>HOME</b></v-tab>
          <v-tab><b>PROFILE</b></v-tab>
          <v-tab><b>LOGIN</b></v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
</div>
  <!-- Sizes your content based upon application components -->


    <!-- Provides the application the proper gutter -->
    <v-content>
      <nuxt/>
  </v-content>
  
  
 <v-footer color="#fccd14"
    dark
    padless
  >
    <v-card 
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn 
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        ************ Chaiyaphum Technical College ***********
        
      </v-card-text>

      <v-divider></v-divider>

    
    </v-card>
  </v-footer>
</v-app>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
  }
</script>

