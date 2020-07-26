<template>
 <v-app>
   <v-card color="#02b4f4">
       <v-card-title>
         <h1>Register</h1>
       </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field  prepend-icon="accessibility" label="name" />
         <v-text-field  prepend-icon="call" label="phone number" />
         <v-text-field  prepend-icon="account_balance" label="address" />
         <v-text-field  prepend-icon="mdi-account-circle" label="Username" />
         <v-text-field 
            :type="showPassword ? 'text' : 'password'" 
            label="Password"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
         <v-card-actions>
         <center>
         <nuxt-link to="/login"><v-btn @click="confirm" color="warning" dark large>CONFIRM</v-btn></nuxt-link>
         <nuxt-link to="/login"><v-btn @click="cancel" color="error" dark large>CANCEL</v-btn></nuxt-link>
         </center>
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