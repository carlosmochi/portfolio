<template>
  <Header/>
  <nav>
    <router-link to="/">Projetos</router-link> |
    <router-link to="/about">Sobre mim</router-link>
  </nav>
  <router-view/>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import Header from '@/components/Header.vue';
  // import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

  export default defineComponent({
    name: 'HomeView',
    components: {
      Header,
    },
  });
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 20px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
