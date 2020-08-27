<template>
  <center>
    <br>
    <v-card width="500" color="teal orange darken-4">
      <v-card-title-center>
        <v-icon size="100" color="yellow accent-3">
          important_devices
        </v-icon>
        <h5>ระบุชื่อผู้ใช้และหรัสผ่านก่อนเข้าสู่ระบบ{{ gpa }}</h5>
      </v-card-title-center>
      <v-card-text>
        <v-form>
          <v-text-field label="รหัสจังหวัด" v-model="province_code"
                        prepend-icon="mdi-account-circle"
          />
        </v-form>
      </v-card-text>
      <v-card-actions>
        <nuxt-link to="register">
          <v-btn class="ma-2" tile color="amber accent-3" dark>
            REGISTER
          </v-btn>
        </nuxt-link>
        <v-spacer />
        <v-btn class="ma-2" tile color="amber accent-3" dark @click="doSearch">
          LOGIN
        </v-btn>
        </v-btn>
        </v-btn>
      </v-card-actions>
    </v-card>
  </center>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      province_name: '',
      province_code: '',
      school: '',
      user: '',
      password: '',
      gpa: '',
    }
  },
  methods: {
    async doSearch() {
      console.log('do search  province')
      let res = await fetch('http://localhost:7001/form10?province_code=' + this.province_code)
      let data = await res.json()
      console.log(data.rows[0][0].province_name)
      this.province = data.rows[0].province_name;
    },
  },
}
</script>