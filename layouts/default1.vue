<template>
<div>
<v-app>
  <v-app-bar color="#02b4f4"densedark>
       <v-app-bar-nav-icon></v-app-bar-nav-icon>
         <v-toolbar-title>Title</v-toolbar-title>
            <v-spacer></v-spacer>
               <v-btn icon>
                  <v-icon>mdi-heart</v-icon>
               </v-btn>
               <v-btn icon>
                  <v-icon>mdi-magnify</v-icon>
               </v-btn>
                  <v-menu leftbottom>
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn icon v-bind="attrs"v-on="on">
                        <v-icon>mdi-dots-vertical</v-icon>
                      </v-btn>
                    </template>
                    <v-list>
                      <v-list-item v-for="n in 5":key="n"@click="() => {}">
                        <v-list-item-title>Option {{ n }}</v-list-item-title>
                      </v-list-item>
                    </v-list>
                  </v-menu>
  </v-app-bar>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

  <v-footer>
    <!-- -->
  </v-footer>
</v-app>
</div>
</template>