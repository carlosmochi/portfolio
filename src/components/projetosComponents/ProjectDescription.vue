<template>
    <div class="project_description">
        <div class="description_img">
            <img v-bind:src="projectImage" />
        </div>
        <div class="description_text">
            <a>{{ projectDescription }}</a>
            <a class="page_link" :href="projectLink" target="_blank">{{ projectLink }}</a>
        </div>
    </div>
</template>

<script>
    import { defineComponent } from 'vue';

    export default defineComponent({
    name: 'ProjectDescription',
    props:{
        projectDescription: String,
        projectLink: String,
        projectImage: String,
    },
    });
</script>