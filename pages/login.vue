<template>
 <v-app>
   <v-card color="#02b4f4">
       <v-card-title>
         <h1>Login</h1>
       </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field  prepend-icon="mdi-account-circle" label="Username" />
         <v-text-field 
            :type="showPassword ? 'text' : 'password'" 
            label="Password"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
         <v-card-actions>
         <nuxt-link to="/register"><v-btn @click="register" color="success" dark large>REGISTER</v-btn></nuxt-link>
          <v-spacer></v-spacer>
         <nuxt-link to="/"><v-btn @click="doLogin" color="warning" dark large>LOGIN</v-btn></nuxt-link>
         </v-card-actions>
       </v-form>
     </v-card-text>
   </v-card>
 </v-app>
</template>
<script>
export default {
  name: 'App',
  data () {
    return {
      showPassword: false
    }
  }
}
</script>