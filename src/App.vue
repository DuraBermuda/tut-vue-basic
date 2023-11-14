<template>
  <h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>
</template>
  
<script>

export default {
  name: 'App',
  data() {
    return {
      fullNames: [
        { first:'Bruce', last:'Wayne'},
        { first:'Clark', last:'Kent'},
        { first:'Princess', last:'Diana'},
        ]
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
