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
  import { initializeApp } from "firebase/app";
  import { getAnalytics } from "firebase/analytics";

  import Header from '@/components/Header.vue';
  // import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

  const firebaseConfig = {
    apiKey: "AIzaSyCfCqunOLZ4P6Ub9J1cznrS1U4njhGxYg4",
    authDomain: "portfolio-6ecad.firebaseapp.com",
    projectId: "portfolio-6ecad",
    storageBucket: "portfolio-6ecad.appspot.com",
    messagingSenderId: "715389661062",
    appId: "1:715389661062:web:e44ddc9dff092a964e0607",
    measurementId: "G-4P80Q2335X"
  };

  const app = initializeApp(firebaseConfig);
  const analytics = getAnalytics(app);

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
