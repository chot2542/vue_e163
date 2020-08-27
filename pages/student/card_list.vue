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
            text: 'ID',
            align: 'start',
            sortable: false,
            value: 'id',
          },
          { text: 'CARD_CODE', value: 'card_code' },
          { text: 'สถานะบุคคล', value: 'ref_type' },
          { text: 'CODE', value: 'ref_code' },
          { text: 'สถานะ', value: 'is_active' },
        ],
        desserts: [
        ],
      }
    },
    created(){
        this.listCard()
    },
    methods:{
      async  listCard(){
            let res = await fetch('http://localhost:7001/listCard')
            let data = await res.json()
            console.log(data)
            this.desserts = data.rows[0];
         }
    }
  }
</script>