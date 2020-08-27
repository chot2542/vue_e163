<template>
 <v-app>
   <v-card color="#7c7c79">
       <v-card-title>
         <span style="font-size: 100px" class="material-icons">lock</span>
         <h1>Login {{gpa}}</h1>
       </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field   v-model="user" prepend-icon="mdi-account-circle" label="Username"/>
         <v-text-field 
            :type="showPassword ? 'text' : 'password'" 
            label="Password"
            v-model="password"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
         <v-card-actions>
         <nuxt-link to="/register"><v-btn @click="register" color="success" dark large>REGISTER</v-btn></nuxt-link>
          <v-spacer></v-spacer>
         <v-btn @click="doSave" color="warning" dark large>LOGIN</v-btn>
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
      showPassword: false,
      user: '',
      password: '',
      gpa:'',
    }
  },
  methods:{
   async doSave(){
      console.log("do save")
      console.log("user:", this.user)
      console.log("password:", this.password)
      //this.$router.push('/#/')
      let res = await fetch('http://localhost:7001/list?user='+this.user)
      let data = await res.json()
      console.log("data=", data.data[0].GPA);
      this.gpa = data.data[0].GPA;
    }
  },
}
</script>