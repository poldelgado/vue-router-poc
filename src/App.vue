<template>
  <div id="app">
    <div id="nav">
      <p class="logo">Travel App</p>
      <ul class="nav-links">
        <li class="links">
          <router-link to="/home">
            Home
          </router-link>
        </li>
        <li v-for="destination in destinations"
          :key="destination.name"
          class="links">
          <router-link :to="{
            name: 'DestinationDetails',
            params: {id:destination.id}
          }">
            {{ destination.name }}
          </router-link>
        </li>
      </ul>
    </div>
    <router-view />
  </div>
</template>

<script>
import store from "@/store";
export default{
  data() {
    return {
      destinationId: this.$route.params.id,
      destinations: store.destinations,
    };
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
}

#nav {
  display:flex;
}

#nav a {
  color: #2c3e50;
  text-decoration: none;
  font-weight: bold;
}

.logo {
  font-size: 20px;
  color: purple;
  font-weight: bold;
}
.links {
  padding-right: 20px;
  list-style: none;
}
.links:hover {
  text-decoration: underline;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
