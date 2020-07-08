<template>
  <div>
    <h2>Hello: {{ name }}</h2>
    <h2>age: {{ age }}</h2>
    <input type="text" v-model="name">
    <input type="text" v-model="age">
    <center>
    <p>    
    <div><v-btn @click="doSave" color="error" dark large>SAVE</v-btn></div>
    <p>
    <div><v-btn @click="doHome" color="warning" dark large>HOME</v-btn></div>
    <p>
    <div><v-btn @click="doMenu" color="success" dark large>MAIN MENU</v-btn></div>
    </center>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "Aekachot Ngamsombut",
      age: 20,
    }
  },
  methods:{
      doSave(){
      console.log("DO SAVE");    
      },
      doMenu(){
      this.$router.replace('menu');  
      },
      doHome(){
      this.$router.push('/');      
      },
    },
}
</script>