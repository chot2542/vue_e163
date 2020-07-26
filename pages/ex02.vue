<template>
  <div>
    <h1>HELLO {{name}}</h1>
    <input type="text" value="dep">
   <v-col cols="12" sm="6" md="4">
          <v-text-field
            label="Filled"
            filled
            dense
          ></v-text-field>
        </v-col>
        
        <v-col cols="12" sm="6" md="4">
          <v-text-field
            label="Outlined"
            placeholder="Placeholder"
            outlined
            dense
          ></v-text-field>
        </v-col>


         <v-text-field
            label="Prepend inner"
            prepend-inner-icon="mdi-map-marker"
          ></v-text-field>
          
  </div>  
</template>
<script>
export default {
  data:function(){
    return{
     name:"Aekachot",
     age:20,
     dep:"information  technology",
     first:"chaiyaphum",
    }
  }
}
</script>
