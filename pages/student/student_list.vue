<template>
  <v-data-table
    :headers="headers"
    :items="desserts"
    :sort-by="['calories', 'fat']"
    :sort-desc="[false, true]"
    multi-sort
    class="elevation-1"
  ></v-data-table>
</template>
<script>
  export default {
    data () {
      return {
        headers: [
          {
            text: 'std_id',
            align: 'start',
            sortable: false,
            value: 'code',
          },
          { text: 'ชื่อ - สกุล', value: 'first_name' },
          { text: 'สถานะ', value: 'is_active' },
        ],
        desserts: [
          {
            std_id: '6239010004',
            fname: 'นายณัฐพล ขอพ่วงกลาง',
            status: 'เปิดใช้งาน',
          },
          {
            std_id: '6239010015',
            fname: 'นายเอกโชติ งามสมบัติ',
            status: 'ระงับการใช้งาน',
          },

        ],
      }
    },
    created(){
        this.listStd()
    },
    methods:{
      async  listStd(){
            let res = await fetch('http://localhost:7001/listStd')
            let data = await res.json()
            console.log(data)
            this.desserts = data.rows[0];
         }
    }
  }
</script>