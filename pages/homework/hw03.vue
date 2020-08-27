<template>
  <v-card color="blue" dark>
    <center>
      <v-icon size="120">account_balance</v-icon>
      <br />
      <font face="TH SarabunPSK" style="font-size: 25px;">ข้อ 3 อยากทราบว่านักศึกษาอยู่วิทยาลัยอะไร</font>
    </center>

    <v-card-text>
      <v-form>
        <v-text-field v-model="student_id" prepend-icon="mdi-account-circle" label="รหัสนักศึกษา" />
        <v-text-field
          v-model="school_name"
          prepend-icon="mdi-account-circle"
          label="๊ชื่อสถานศึกษา"
        />
      </v-form>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn rounded color="warning" dark @click="form3">ค้นหา</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      showPassword: false,
      student_id: '',
      school_name: '',
    }
  },
  methods: {
    async form3() {
      console.log("Success Form3");
      console.log("user:", this.student_id);
      //this.$router.push('/register')
      let res = await fetch('http://localhost:7001/form3?student_id=' + this.student_id)
      let data = await res.json()
      this.student_id = data.data[0].student_id
      this.school_name = data.data[0].school_name
    },
  },
};
</script>