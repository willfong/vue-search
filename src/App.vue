<template>
  <div id="app">
    <h1>Vue Search String</h1>
    <input v-model="searchString" />
    <p>{{results}}</p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      myList: ['Will', 'Jasmine', 'Shanhan', 'Rachel'],
      searchString: '',
    }
  },
  computed: {
    results() {
      return this.myList.filter(r => r.toLowerCase().includes(this.searchString.toLowerCase()));
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
