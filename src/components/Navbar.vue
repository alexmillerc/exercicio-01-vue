<template>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
</template>

<script>
export default {
  name: 'Navbar',
  data(){
    return {
      items: ['Section 1', 'Section 2', 'Section 3', 'Section 4']
    }
  }
}
</script>

<style scoped>
  ul{
    display: flex;
    list-style-type: none;
    justify-content: space-around;
    padding: 2% 15%;
    background-color: #f0a500;
    color: #1e2022;
  }
</style>