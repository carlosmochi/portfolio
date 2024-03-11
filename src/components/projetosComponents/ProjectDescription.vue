<template>
    <div class="project_description">
        <div class="description_img">
            <img v-bind:src="projectImage" />
        </div>
        <div class="description_text">
            <a>{{ projectDescription }}</a>
        </div>
    </div>
</template>

<script>
    import { defineComponent } from 'vue';

    export default defineComponent({
    name: 'ProjectDescription',
    props:{
        projectDescription: String,
        projectImage: String,
    },
    });
</script>