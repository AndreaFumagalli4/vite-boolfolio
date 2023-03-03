<script>
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';

export default{
    name: 'AppMain',

    components:{
        ProjectCard,

    },

    data() {
        return {
            apiUrl: 'http://127.0.0.1:8000/api/projects',
            projects: [],
        }
    },

    methods: {
        getProjects(){
            axios.get(this.apiUrl, {
                params: {
                }
            })
            .then((response) => {
                this.projects = response.data.results.data;
                console.log(this.projects);
            })
            .catch(function (error) {
                console.warn(error);
            });
        }
    },

    created(){
        this.getProjects();
    }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1 class="fs-3">
                        My projects:
                    </h1>
                </div>
            </div>
            <div class="row">
                <ProjectCard v-for="project in projects"
                :projectId="project.id"
                :projectTitle="project.title"
                :projectImage="project.thumb"
                :projectType="project.type.name"
                :projectTechnologies="project.technologies"/>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">

</style>