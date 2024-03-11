<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
    <Projetos />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import Projetos from '@/components/Projetos.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
    HelloWorld,
    Projetos,
  },
});

</script>

