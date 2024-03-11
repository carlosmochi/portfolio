<template>
   <div class="project_selection">
      <ul>
         <li 
         v-for="project in projectData"> 
         <button v-on:click="selectProject(project)" :class="{selected: project.isSelected}" class="project_button">{{ project.projectTitle }}</button></li>
      </ul>
   </div>
</template>

<script>
   import { defineComponent } from 'vue';

    export default defineComponent({
      name: 'ProjectSelection',
      props:{
         projectData: Array,
      },
      methods:{
         selectProject(value){
            for (let i = 0; i < this.projectData.length; i++) {
               this.projectData[i].isSelected = false
               
            }
            value.isSelected = !value.isSelected;
            this.$emit('select-project', value)
         }
      }
    });
</script>