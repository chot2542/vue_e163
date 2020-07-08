<template>
  <div>
    <h2>Hello: {{ name }}</h2>
    <h2>age: {{ age }}</h2>
    <input type="text" :value="name">
    <input type="text" v-model="name">
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
}
</script>