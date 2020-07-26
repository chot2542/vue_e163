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
     <v-app-bar
      color="primary"
      dense
      dark
    >
       <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Destinations</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

     <br>
     
    <v-container>
      <v-row dense>
        <v-col cols="12">
          <v-card color="#bcbbb8"dark>
            <center>
                <br>
                <br>
              <h2>Wonderful Mexico</h2>
            <v-card-subtitle>19 Photos</v-card-subtitle>
              <br>
            </center>
          </v-card>
        </v-col>

        <v-col cols="12">
          <v-card color="#bcbbb8"dark>
            <center>
                <br>
                <br>
              <h2>Treasure of Egypt</h2>
            <v-card-subtitle>19 Photos</v-card-subtitle>
              <br>
            </center>
          </v-card>
        </v-col>

        <v-col cols="12">
          <v-card color="#bcbbb8"dark>
            <center>
                <br>
                <br>
              <h2>Love in Paris</h2>
            <v-card-subtitle>19 Photos</v-card-subtitle>
              <br>
            </center>
          </v-card>
        </v-col>
 

      </v-row>
    </v-container>
  </v-card>

</div>
  <!-- Sizes your content based upon application components -->


    <!-- Provides the application the proper gutter -->
    
    

</v-app>
</template>
<script>
  export default {
    data: () => ({
      items: [
        {
          color: '#1F7087',
          src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
          title: 'Supermodel',
          artist: 'Foster the People',
        },
        {
          color: '#952175',
          src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
          title: 'Halcyon Days',
          artist: 'Ellie Goulding',
        },
      ],
    }),
  }
</script>

