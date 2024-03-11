<template>
    <div class="project_main_div">
        <ProjectSelection 
        :projectData = projects 
        v-on:select-project="displayProject"/>
        <ProjectDescription 
            :projectDescription = selectedProject.textDescription
            :projectImage = selectedProject.imagePreview />
    </div>
</template>

<script>
import { defineComponent } from 'vue';
import ProjectDescription from '@/components//projetosComponents/ProjectDescription.vue';
import ProjectSelection from '@/components//projetosComponents/ProjectSelection.vue';
import json from '@/assets/data.json'

export default defineComponent({
  name: 'HelloWorld',
  components:{
    ProjectDescription,
    ProjectSelection,
  },
  data() {
    return{
      projects: [],
      selectedProject: {}
    }
  },
  methods: {
    displayProject(project) {
      this.selectedProject = project
    },
    extractProjectsFromJson(){
      this.projects = json
    }
  },
  mounted() {
    this.extractProjectsFromJson()
    this.displayProject(this.projects[0])
  }

});
</script>

<style>
    @import "./styles/Projetos.css";

</style>