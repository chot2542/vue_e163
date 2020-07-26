<template>
 <div>
   <center>
   <v-app>
  <v-container fluid class="pa-0">
    <v-row align="center">
      <v-col cols="12" sm="6">
        <div class="text-center">
          <div class="my-2">
            <nuxt-link to="/activity/homeroom"><v-btn color="primary" dark large>กิจกรรมโฮมรูม</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/special"><v-btn color="error" dark large>กิจกรรมพิเศษ/จิตรอาสา</v-btn></nuxt-link>
          </div>
          <div class="my-2">
            <nuxt-link to="/activity/line"><v-btn color="warning" dark large>กิจกรรมวิชาชีพ</v-btn></nuxt-link>
            <div class="my-2">
            <nuxt-link to="/activity/flag"><v-btn color="success" dark large>กิจกรรมเข้าแถวหน้าเสาธง</v-btn></nuxt-link>
          </div>
          </div>
          <div class="my-2">
            <nuxt-link to="/"><v-btn color="secondary" dark large>กลับสู่หน้าหลัก</v-btn></nuxt-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
  </v-app>
   </center>
 </div>
</template>