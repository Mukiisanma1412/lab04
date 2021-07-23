<template>
  <div id="nav">
    <router-link :to="{ name: 'EventList' }">Home</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link> |
    <router-link :to="{ name: 'EventList', query: { limit: 1 } }" >Size 1</router-link> |
    <router-link :to="{ name: 'EventList', query: { limit: 3 } }">Size 3</router-link>
  </div>

  <!-- new element -->
  <router-view />
</template>

<script>

export default {
  data() { return {
    fonSize: 1
  }},
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
h4 {
  font-size: 20px;
}
</style>
