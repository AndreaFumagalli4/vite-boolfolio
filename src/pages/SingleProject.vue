<script>
import axios from 'axios';
import ProjectCard from '../components/ProjectCard.vue';

export default {
    nama: 'SingleProject',

    components: {
        ProjectCard,
    },

    data() {
        return {
            apiUrl: "http://127.0.0.1:8000",
            project: null,
        }
    },

    methods: {
        getProject(){
            axios.get(this.apiUrl + `/api/projects/${this.$route.params.id}`, {
                params: {
                }
            })
            .then((response) => {
                this.project = response.data.results.data;
                console.log(this.project);
            })
            .catch(function (error) {
                console.warn(error);
            });
        }
    },

    created(){
        this.getProject();
    }
}
</script>

<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12">
                <h1 class="fs-3">
                    Single project whit ID {{this.$route.params.id}}
                </h1>
            </div>
        </div>
        <div class="row">
            <ProjectCard :project="project" />
        </div>
    </div>
</template>

<style scoped lang="scss">
    
</style>