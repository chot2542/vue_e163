<template>
  <div>
    <h1>Student List</h1>
    <ul>
      <li v-for="st in student" :key="st.code">
        <span>{{ st.GPA }}</span>
        <span>{{ st.name }}</span>
        <span>{{ st.lastname }}</span>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      student: [],
    }
  },
   methods: {
    async  listStudent() {
        console.log('list_std')
        let res = await fetch('http://localhost:7001/liststd')
        let data = await res.json()
        console.log('data',data.rows[0])
        this.student = data.rows[0]
   }
  },
    created () {
        this.listStudent()
  },
}
</script>