<template>
    <!-- App.vue -->

<v-app>

    <v-system-bar
          color="#1c81ce"
          :height="height"
          :lights-out="lightsOut"
          :window="window"
        >
          <v-spacer></v-spacer>
          <v-icon>mdi-wifi-strength-4</v-icon>
          <v-icon>mdi-signal-cellular-outline</v-icon>
          <v-icon>mdi-battery</v-icon>
          <span>12:30</span>
        </v-system-bar>
        
  <v-navigation-drawer app>
    <!-- -->
  </v-navigation-drawer>

<div>
     <v-app-bar color="primary"densedark>
      
            <v-btn icon>
              <v-icon>mdi-arrow-left</v-icon>
            </v-btn>

            <v-toolbar-title>Welcome</v-toolbar-title>

            <v-spacer></v-spacer>

            <v-btn icon >
              <v-icon>mdi-magnify</v-icon>
            </v-btn>
            <v-btn icon >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
         
         <template v-slot:extension>
            <v-tabs dark background-color="primary"grow>
      <v-tab>
          SIGN UP
      </v-tab>

      <v-tab>
          SIGN IN
      </v-tab>
    </v-tabs>
    </template>
    </v-app-bar>
</div>
  <!-- Sizes your content based upon application components -->


    <!-- Provides the application the proper gutter -->
    
    <v-content style="padding-top:50px">
        <center>
          <img  style="width: 100px; height: 100px; border-radius: 50%;" 
          src="../img/pro.jpg" width="50">
        
         <v-col style="padding-top:50px;padding-left:30px;padding-right:30px;"cols="12" sm="6">
          <v-text-field 
            v-model="last"
            label="Username"
            solo-inverted
          ></v-text-field>
        </v-col>

          <v-col style="padding-left:30px;padding-right:30px;position:relative; top:-35px;"cols="12" sm="6">
          <v-text-field
            v-model="last"
            label="Password"
            solo-inverted
          ></v-text-field>
        </v-col>
        
        </center>
        <v-checkbox style="padding-left:30px;position:relative; top:-75px;" 
        v-model="hover" label="Remember me" hide-details></v-checkbox>
  
        <center><nuxt-link to=""><v-btn style="padding-left:145px;padding-right:145px;"
        @click="doLogin" color="primary" dark large>Sign In</v-btn></nuxt-link></center>
  </v-content>
  
  
  

</v-app>
</template>

